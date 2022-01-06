# sleepDebtCalculator.js
A simple sleep debt calculator made in JavaScript under a codecademy's project! 

// Sleep Debt Calculator
// Accepts day as an argument to return the # of hours slept that day
const getSleepHours = day => {
  if (day === 'monday') {
    return 7;
  } else if (day === 'tuesday') {
    return 5;
  } else if (day === 'wednesday') {
    return 6;
  } else if (day === 'thursday') {
    return 7;
  } else if (day === 'friday') {
    return 8;
  } else if (day === 'saturday') {
    return 7
  } else if (day === 'sunday') {
    return 8;
  }
};
// console.log(getSleepHours('sunday'));

// Adds hours slept for every da of the week
const getActualSleepHours = () => 7 + 5 + 6 + 7 + 8 + 7 + 8;


/* 
const getActualSleepHours = () => 
getSleepHours('monday') + 
getSleepHours('tuesday') + 
getSleepHours('wednesday') + 
getSleepHours('thursday') + 
getSleepHours('friday') + 
getSleepHours('saturday') + 
getSleepHours('sunday');
console.log(getActualSleepHours());
*/

// stores preferred hours of sleep per week
const getIdealSleepHours = idealHours => idealHours * 7;

/*
const getIdealSleepHours= () => {
  let idealHours = 8;
  return (idealHours * 7);
};
console.log(getIdealSleepHours());
*/

// Calcuates sleep debt and outputs if you are on track or not
const calculateSleepDebt = () => {
  let actualSleepHours = getActualSleepHours();
  let idealSleepHours = getIdealSleepHours(8);
  let overDebt = actualSleepHours - idealSleepHours
  let underDebt = idealSleepHours - actualSleepHours
  if (actualSleepHours === idealSleepHours) {
    console.log('You got the perfect amount of sleep!');
  } else if (actualSleepHours > idealSleepHours) {
    console.log('You got more sleep than needed by ' + underDebt +' hours!');
  } else if (actualSleepHours < idealSleepHours) {
    console.log('You should get some rest! you\'re under your goal by ' + underDebt + ' hours!');
  }
};
// Diplays sleep debt to the screen
calculateSleepDebt();
