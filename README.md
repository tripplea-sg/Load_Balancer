# How to use Load Balancer for MySQL DB System

## Preparation

Please go to MySQL DB System and open your database as follow. Take note private IP Address carefully, you will need that to configure the Load Balancer to point to your MySQL DB System.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/preparation.png)

## Create Load Balancer

### 1. From the console main menu on the left side select *Networking >> Load Balancers*.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/1.png)

### 2. It will bring you to the Load Balancers creation page. Look at the compartment selector on the left and check that you are using the same compartment used to create the VCN and the Compute Instance. Once done, click on *Create Load Balancer*.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/2.png)

### 3. Select the Load Balancer and click button *“Create Load Balancer”*

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/3.png)

### 4. It will bring you to *“Add Details”* tab (see on the left). Set *“Load Balancer Name”* to *LB_Heatwave*.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/4.png)

### 5. Scroll down until you find networking setup on the bottom of the page. Choose *“analytics_vcn_test”* for Virtual Cloud Network, and choose Public subnet *“Public Subnet-analytics_vcn_test (Regional)”&. Do not choose Private subnet, or else you cannot connect to MySQL DB System from OAC. Click *“Next”* to continue.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/5.png)

### 6. It will bring you to *“Choose Backends”* tab (see on the left). Select the *“IP Hash”* box, set protocol to *“TCP”*, and set port to *“3306”*. Click *“Next”* to continue.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/6.png)

### 7. It will bring you to *“Configure Listener”* tab (see on the left). Select the *“TCP”* box and set port to *“3306”*. Click *“Next”* to continue.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/7.png)

### 8. It will bring you to “Managing Logging” tab (see on the left). Leave everything as default. Click “Submit” to create the Load Balancer.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/8.png)

### 9. The Load balancer will have *CREATING* state (as per picture below).

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/9.png)

### 10. Wait a moment until The Load balancer is on *ACTIVE* state (as per picture below).

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/10.png)

### 11. Scroll down this page until you see list of *“Resources”* on the left. Click *“Backend Sets (1)”*.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/11.png)

### 12. You will see a backend set already configured by default. Click that *“backend set”* to continue.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/12.png)

### 13. It will bring you to the *“Backend Set”* setting. Click *“Backends (0)”* to create continue.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/13.png)

### 14. Click *“Add Backends”* to register your MySQL DB System.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/14.png)

### 15. Choose *“IP Addresses”*. Set *“IP Addresses”* to your MySQL DB System’s private IP Address. Set *“Port”* to *3306*. Click button *“Add”* to continue.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/15.png)

### 16. Click button *“Close”* on the following dialog box.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/16.png)

### 17. You will see a backend is added to the backend set (see picture below), and that’s your MySQL DB System. The Backend will have *PENDING* state (as per picture below).

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/17.png)

### 18. *Wait* a moment until The Backend is on *OK* state (as per picture below).

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/18.png)

### 19. Click *“Load Balancers”* link to go back to the Load Balancer creation page.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/19.png)

### 20. Note the *Public IP Address* of your load balancer. You may need this when configuring data set on OAC.

![Image of Yaktocat](https://github.com/tripplea-sg/Load_Balancer/blob/main/20.png)
