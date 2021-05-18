
# Example of importing a 3scale custom metric policy

SERVICE_ID = you need to set the 3scale service identifier

**3scale toolbox commands:**

    • 3scale policies export -f custommetric.json -o json quitala api
    • 3scale policies import -u https://raw.githubusercontent.com/sgutierr/3scaledemo/master/policies/custommetric.json quitala customer_management__v4_0_0_
    • 3scale metric create --description Status_2XX -t Status_2XX quitala $SERVICE_ID Status_2XX
    • 3scale metric create --description Status_4XX -t Status_4XX quitala $SERVICE_ID Status_4XX
    • 3scale metric create --description Status_5XX -t Status_5XX quitala $SERVICE_ID Status_5XX
    • 3scale metric create --description Linux_x86_64 -t Linux_x86_64 quitala $SERVICE_ID Linux_x86_64
    • 3scale metric create --description Postman -t Postman quitala $SERVICE_ID Postman
    • 3scale metric create --description curl -t curl quitala $SERVICE_ID curl   
    









