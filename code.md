/*WARM UP 🏋️‍♂️ convert each of the commented out functions below to arrow functions*/
// let myFunction = function () {
// console.log("Function was invoked!");
// };
// myFunction();
let myFunction = () => console.log('function was invoked!');
myFunction();
// let anotherFunction = function (param) {
//   return param;
// };
// anotherFunction("Example");
let anotherFunction = (param) => param;
console.log(anotherFunction('hello'));
// let add = function (param1, param2) {
//   return param1 + param2;
// };
// add(1,2);
let add = (param1, param2) => param1 + param2;
console.log(add(1,3));
// let subtract = function (param1, param2) {
//   return param1 - param2;
// };
// subtract(1,2);
let subtract = (param1, param2) => param1 - param2;
console.log(subtract(5,2));
/* Work out 💪 */
/* TASK 1 🚀 
// Dollars to Euros - write a function that will take an amount of dollars (USD) and change it  into euros (EUR) - with the current exchange rate 1 USD === .85 EUR */
function convertToEuro(dollar){
  return dollar * 0.85;
}
console.log(convertToEuro(1));
/* TASK 2 🚀 
// Take the function above a step further - you have dollars and you are visiting the following 5 countries: Britan, Germany, Turkey, Bulgaria and Ukraine - you need to write a function that will take a dollar amount, and a country and return the exchange rate for that country - the function should return a string that says `your exchange rate for dollarAmount dollars in country will be exchangeRate currencyInitals ` If the country is not on your list your string should return 'that country is not on your list'
// 1 usd === 0.85 euro
// 1 usd === 0.77 British Pounds
// 1 usd === 6.96 Turkish Lira 
// 1 usd === 1.66 Bulgarian Lev 
// 1 usd === 27.7 Ukrainian hryvnia */
function convertCurrency(dollarAmount, country){
  if(country === 'Germany'){
    let exchange =  dollarAmount * 0.85;
    return `your exchange rate for ${dollarAmount} dollars in ${country} will be ${exchange} EUR `;
  }else if(country === 'Britan'){
    let exchange =  dollarAmount * 0.77;
    return `your exchange rate for ${dollarAmount} dollars in ${country} will be ${exchange} Pound Sterling`;
  }else if(country === 'Turkey'){
    let exchange =  dollarAmount * 6.69;
    return `your exchange rate for ${dollarAmount} dollars in ${country} will be ${exchange} Lira`;
  }else if(country === 'Bulgaria'){
    let exchange =  dollarAmount * 1.66;
    return `your exchange rate for ${dollarAmount} dollars in ${country} will be ${exchange} Lev`;
  }else if(country === 'Ukraine'){
    let exchange =  dollarAmount * 27.7;
    return `your exchange rate for ${dollarAmount} dollars in ${country} will be ${exchange} Hryvnia`;
  }else{
    return `your country is not on the list`;
  }
}
console.log(convertCurrency(10, 'Ukraine'));
/*TASK 3 🚀
/// Write a function that takes an airport code and returns the city, country of that airport 
// find the following codes AAA, ABZ, ABX, ABT, ACA */
function airportCode(code){
  for(let i = 0; i < airports.length; i++){
    if(code === airports[i]['code']){
      console.log(`this airport is in ${airports[i]['city']}, ${airports[i]['country']}`);
    }
  }
}
airportCode('AAA');
airportCode('ABZ');
airportCode('ABX');
airportCode('ABT');
airportCode('ACA');
/*TASK 4 🚀 
// Write a function to that will find the phone number for an airport in a given city  */
function callMeMaybe(city 'arr){
  for(let i = 0; i < arr.length; i++){
    if(city === arr[i]["city"]){
      return arr[i]["phone"];
    }
  }
}
console.log(callMeMaybe('Allentown'));
/*TASK 5 🚀 
// Write a function that will return all the airports in a given country  */
function gimmeTheAirports(country){
  let options = [];
  for(let i = 0; i < airports.length; i++){
    if(country === airports[i]["country"]){
      options.push(airports[i]["name"]);
    }
  }
  return options;
}
console.log(gimmeTheAirports('United States'));
/*TASK 6 🚀 
// Write a function that takes and airport name and returns the airport code
// find the code for the following airports: Al Baha Airport, Ambler Airport, Abuja International Airport*/
function codeName(airportName){
  for(let i = 0; i < airports.length; i++){
    if(airportName === airports[i]["name"]){
      return airports[i]["code"];
    }
  }
}
console.log(codeName('Al Baha Airport'));
console.log(codeName('Ambler Airport'));
console.log(codeName('Abuja International Airport'));
/*TASK 7 🚀
// Write a function that takes an airport code and returns the number of direct flights available */
function directFlights(code){
  for(let i = 0; i < airports.length; i++){
    if(code === airports[i]["code"]){
      return airports[i][ "direct_flights"];
    }
  }
}
console.log(directFlights('ABZ'));
/*TASK 8 🚀
// Find out what your flight options are - write a function that returns a new array of all the country names in a set of data*/
function tripOptions(arr){
  let countries = [];
  for(let i = 0; i < arr.length; i++){
    countries.push(arr[i]["country"]);
  }
  return countries;
}
console.log(tripOptions(airports));
 