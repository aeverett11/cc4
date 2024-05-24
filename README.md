# Electric Car Class Implementation 
Enhance your understanding of inheritance in object-oriented programming by extending a Car class to create an Electric Car (EV) class. This new class will include additional properties and methods specific to electric vehicles.

function Car(make, speed) {
  this.make = make;
  this.speed = speed;
}

function EV(make, speed, charge) {
  Car.call(this, make, speed);
  this.charge = charge;
}

EV.prototype.chargeBattery = function(chargeTo) {
  this.charge = chargeTo;
};
