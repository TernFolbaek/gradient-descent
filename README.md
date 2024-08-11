## Gradient Descent Summary
### We begin by computing the gradient with respect to our parameters w and b:
### **Compute Gradient**
 - #### Description: Compute gradient returns the gradient for every w parameter and b parameter for each training example, first looping through "m" amount of times, and thereafter a nestood loop of "j" iterations to retrieve the gradient of every feature coefficient. Which looks as following:
     $$\frac{dJ(w,b)^{(i)}}{db} = (f_{w,b}(x^{(i)}) - y^{(i)})$$

     $$\frac{dJ(w,b)^{(i)}}{dw} = (f_{w,b}(x^{(i)}) - y^{(i)})x_j^{(i)}$$
   #### And at last return the total gradient from all training examples:
   $$\frac{\partial J(w,b)}{\partial b}  = \frac{1}{m} \sum\limits_{i = 0}^{m-1} \frac{\partial J(w,b)}{\partial b}^{(i)}$$
    
    $$\frac{\partial J(w,b)}{\partial w}  = \frac{1}{m} \sum\limits_{i = 0}^{m-1} \frac{\partial J(w,b)}{\partial w}^{(i)}$$

### Thereafter can we apply our newfound gradient values into the gradient descent process:
 
### **Gradient descent**
  - #### Description: Gradient descent is then iteratively used to find the optimal w,b parameter values. It does this by iterating x amount of times, starting with updating the gradient of each parameter, thanks to the "compute gradient" function. Thereafter w, and b parameters are updated as following:
      $$w = w-\alpha *  \frac{\partial J(w,b)}{\partial w}$$
      $$b = w-\alpha *  \frac{\partial J(w,b)}{\partial b}$$
    #### in this case the "=" is not used as the equality sign, but as the assignment operator. w is an array in this case, where its dimension "n" is corresponds to quantity of features.
