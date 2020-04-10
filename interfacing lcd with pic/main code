#include "mcc_generated_files/mcc.h"
#include"Motors.h"
#include "Hc_Sr05.h"
#include"Esp_8266.h"
#include"LCD.h"


/*
                         Main application
 */
 
void main(void)
{
    // Initialize the device
    SYSTEM_Initialize();
    char rec[100], Direction;
    float  Distance=0, Time=0;
    Lcd_Start();
    Lcd_Set_Cursor(1,1); //cursor goes to first line and first character
    Lcd_Print_String("Group 7 Project"); //what we want to print on screen
    Lcd_Set_Cursor(2,2);  //cursor goes to second line and first character
    Lcd_Print_String("7 April 2020"); //what we want to print on screen
    // __delay_ms(900);
   // __delay_ms(900);
   
  /*  esp8266_isStarted();
   
    esp8266_mode(1);
    __delay_ms(10);
    esp8266_connect("Kajal","KajalKajal");
    __delay_ms(10);
    esp8266_start("TCP","api.thingspeak.com","80");
    __delay_ms(10);
   */
   
   
      /* esp8266_send("Kajal,KajalKajal");
      esp8266_send("GET /update?api_key=231FL6YWUTJLN6BR&field1=88.9990");
       esp8266_send("GET /update?api_key=231FL6YWUTJLN6BR&field1=88.9990");
   esp8266_send("GET /update?api_key=231FL6YWUTJLN6BR&field1=88.9990");
    __delay_ms(10);
    */
    //BUZZER_SetHigh();
     //__delay_ms(500);  
    /*Esp_data("AT\r\n") ;
    Esp_data("AT+CWMODE=1\r\n");
    Esp_data("AT+CJWAP=\"Kajal\",\"KajalKajal\"\r\n");
   
   
     Esp_data("AT+CIPMUX=1\r\n");
    Esp_data("AT+CIPSTART=0,\"TCP\",\"api.thingspeak.com\",""80");
    */
   
    //Chair_Position("FORWARD");
    while (1)
    {
   /*     __delay_ms(900);
        __delay_ms(900);
             esp8266_send("GET /update?api_key=231FL6YWUTJLN6BR&field1=33.9990");
         __delay_ms(900);
         __delay_ms(900);
        //Esp_data("AT+CWMODE=""KAJAL"",""\r\n");  
       
        */
       
        if(EUSART1_is_rx_ready()){
            Direction= EUSART1_Read();
       
         
        if(Direction=='F')
            {
                 Chair_Position("FORWARD");
                  __delay_ms(100);
                 // Direction = 'N';
                 // Esp_data("Moving");
            }

            else if(Direction=='B')
            {
                 Chair_Position("BACK");
                  __delay_ms(100);
                  //Direction = 'N';
                  // Esp_data("Back");
            }


            else if(Direction=='L'){
                 Chair_Position("LEFT");
                  __delay_ms(100);
                  //Direction = 'N';
                  // Esp_data("LEFT");

            }
             else if(Direction=='R'){
                 Chair_Position("RIGHT");
                  __delay_ms(100);
                  //Direction = 'N';
                  // Esp_data("RUGHT");

            }
             else if(Direction=='S'){
                 Chair_Position("STOP");
                  __delay_ms(100);
                  //Direction = 'N';
                  // Esp_data("STOP");

             }}
             else
                 Chair_Position("STOP");
       // __delay_ms(900);
       // Chair_Position("FORWARD");
           
         
         
         while(Get_Distance_Front()<=12)
         {
          Chair_Position("STOP");
           BUZZER_SetHigh();                    // Buzzer ON
           __delay_us(200);
         }
       
         while(Get_Distance_Rear()<=12)
         {
          Chair_Position("STOP");
           BUZZER_SetHigh();                    // Buzzer ON
           __delay_us(200);
         }
       
         //BUZZER_SetHigh();
          //__delay_ms(900);
          BUZZER_SetLow();                      // Buzzer OF
         // __delay_ms(900);
    }
}

