<template>
  <h1 style="color: black;">{{ channel }}</h1>
  <div class="calculator">
    <h1 style="color:white"> {{ lastnamd }}</h1>
    <div class="display">
      <input type="text" v-model="displayValue" readonly>
    </div>
    <div class="buttons">
      <button @click="clearDisplay()" class="btn btn-clear">C</button>
      <button @click="appendToDisplay('(')" class="btn">(</button>
      <button @click="appendToDisplay(')')" class="btn">)</button>
      <button @click="appendToDisplay('/')" class="btn btn-operator">÷</button>
      
      <button @click="appendToDisplay('7')" class="btn">7</button>
      <button @click="appendToDisplay('8')" class="btn">8</button>
      <button @click="appendToDisplay('9')" class="btn">9</button>
      <button @click="appendToDisplay('*')" class="btn btn-operator">×</button>
      
      <button @click="appendToDisplay('4')" class="btn">4</button>
      <button @click="appendToDisplay('5')" class="btn">5</button>
      <button @click="appendToDisplay('6')" class="btn">6</button>
      <button @click="appendToDisplay('-')" class="btn btn-operator">-</button>
      
      <button @click="appendToDisplay('1')" class="btn">1</button>
      <button @click="appendToDisplay('2')" class="btn">2</button>
      <button @click="appendToDisplay('3')" class="btn">3</button>
      <button @click="appendToDisplay('+')" class="btn btn-operator">+</button>
      
      <button @click="appendToDisplay('0')" class="btn">0</button>
      <button @click="appendToDisplay('.')" class="btn">.</button>
      <button @click="deleteLastChar()" class="btn btn-delete">←</button>
      <button @click="calculateResult()" class="btn btn-equal">=</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      displayValue: '',
      lastnamd:'Casino',
      channel:'WELCOME TO CASINO'

    };
  },
  methods: {
    appendToDisplay(value) {
      this.displayValue += value;
    },
    clearDisplay() {
      this.displayValue = '';
    },
    deleteLastChar() {
      this.displayValue = this.displayValue.slice(0, -1);
    },
    calculateResult() {
      try {
        this.displayValue = eval(this.displayValue);
      } catch (error) {
        this.displayValue = 'Error';
      }
    }
  }
};
</script>

<style scoped>
.calculator {
  width: 300px;
  margin: 50px auto;
  background-color: #333;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
  font-family: 'Arial', sans-serif;
}

.display {
  margin-bottom: 10px;
}

.display input {
  width: 100%;
  padding: 15px;
  font-size: 1.8rem;
  text-align: right;
  background-color: #666;
  color: white;
  border: none;
  border-radius: 5px;
  box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.5);
  outline: none;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

.btn {
  padding: 20px;
  font-size: 1.2rem;
  background-color: #555;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: #777;
}

.btn:active {
  background-color: #444;
}

.btn-clear {
  grid-column: span 2;
}

.btn-operator {
  background-color: #ff9500;
}

.btn-delete {
  background-color: #ff3b30;
}

.btn-equal {
  background-color: #4cd964;
}
</style>
