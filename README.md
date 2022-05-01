# SIT210-Task3.2C-ParticleIFTTT

#define light_sensor = A0;
#define LIGHT_LEVEL_THRESHOLD 900 

void setup() {
 
} 

void loop() { 
    
 
   int darkness =  random(8, 10) * 200; 
   
   if (darkness >= LIGHT_LEVEL_THRESHOLD) { 
       Particle.publish("changing-light", "dark"); 
       delay(3000);
       
   } else { 
       Particle.publish("light"); 
       delay(3000);
   } 
}
