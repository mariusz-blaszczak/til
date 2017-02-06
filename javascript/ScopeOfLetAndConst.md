# Scope of let and const in new ES6 syntax

Today I learned new thing about scope of let and const. I wrote this code

if (lastStep > this.state.stepNumber) {
let history = this.state.history.slice(0, this.state.stepNumber);
} else {
let history = this.state.history;
}
const current = history[history.length - 1];

and was thinking why in 10. line history is different than this.state.history. And then I found out that I must declare it before if. 

let history;
if (lastStep > this.state.stepNumber) {
history = this.state.history.slice(0, this.state.stepNumber);
} else {
history = this.state.history;
}
const current = history[history.length - 1];