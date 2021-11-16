# How to use Load Balancer for MySQL DB System

### 1. From the console main menu on the left side select *Networking >> Load Balancers*.


### 2. It will bring you to the Load Balancers creation page. Look at the compartment selector on the left and check that you are using the same compartment used to create the VCN and the Compute Instance. Once done, click on *Create Load Balancer*.


### 3. Select the Load Balancer and click button *“Create Load Balancer”*



### 4. It will bring you to *“Add Details”* tab (see on the left). Set *“Load Balancer Name”* to *LB_Heatwave*.


### 5. Scroll down until you find networking setup on the bottom of the page. Choose *“analytics_vcn_test”* for Virtual Cloud Network, and choose Public subnet *“Public Subnet-analytics_vcn_test (Regional)”&. Do not choose Private subnet, or else you cannot connect to MySQL DB System from OAC. Click *“Next”* to continue.


### 6. It will bring you to *“Choose Backends”* tab (see on the left). Select the *“IP Hash”* box, set protocol to *“TCP”*, and set port to *“3306”*. Click *“Next”* to continue.


### 7. It will bring you to *“Configure Listener”* tab (see on the left). Select the *“TCP”* box and set port to *“3306”*. Click *“Next”* to continue.


### 8. It will bring you to “Managing Logging” tab (see on the left). Leave everything as default. Click “Submit” to create the Load Balancer.


### 9. The Load balancer will have *CREATING* state (as per picture below).


### 10. Wait a moment until The Load balancer is on *ACTIVE* state (as per picture below).



### 11. Scroll down this page until you see list of *“Resources”* on the left. Click *“Backend Sets (1)”*.


### 12. You will see a backend set already configured by default. Click that *“backend set”* to continue.


### 13. It will bring you to the *“Backend Set”* setting. Click *“Backends (0)”* to create continue.



### 14. Click *“Add Backends”* to register your MySQL DB System.



### 15. Choose *“IP Addresses”*. Set *“IP Addresses”* to your MySQL DB System’s private IP Address. Set *“Port”* to *3306*. Click button *“Add”* to continue.



### 16. Click button *“Close”* on the following dialog box.



### 17. You will see a backend is added to the backend set (see picture below), and that’s your MySQL DB System. The Backend will have *PENDING* state (as per picture below).


### 18. *Wait* a moment until The Backend is on *OK* state (as per picture below).


### 19. Click *“Load Balancers”* link to go back to the Load Balancer creation page.


### 20. Note the *Public IP Address* of your load balancer. You may need this when configuring data set on OAC.


