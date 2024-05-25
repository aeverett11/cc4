# Electric Car Class Implementation 
Enhance your understanding of inheritance in object-oriented programming by extending a Car class to create an Electric Car (EV) class. This new class will include additional properties and methods specific to electric vehicles.

// Parent class 'Car'
function Car(make, speed) {
  this.make = make;
  this.speed = speed;
  }
  
// Inheriting from 'Car'
EV.prototype = Object.create(Car.prototype);
EV.prototype.constructor = EV;

// 'chargeBattery' method
EV.prototype.chargeBattery = function(chargeTo) {
  this.charge = chargeTo;
  console.log(`${this.make} charged to ${chargeTo}%`);
};
