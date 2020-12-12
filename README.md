#This python code enables one to send a text message/SMS 
#Command 'pip install twilio' may need to be used 
from twilio.rest import Client 
 
account_sid = 'AC52435065aeffd04cb4af5ce07768ca5c' 
auth_token = 'My auth token' #auth token from twilio account
client = Client(account_sid, auth_token) 
 
message = client.messages.create( 
                              from_='+14404269666',#number generated from twilio account
                              body='I cannot believe this works.',        
                              to='My phone number' #phone number fed in here with country code obviously
                          ) 
 
print(message.sid)
