1.We considered the model complexity based on the goodness of fit and used AIC (Akaike Information Criterion) and BIC (Bayesian Information Criterions) to re-evaluate the IDM model and the Sigmoid-IDM model. AIC and BIC are model selection methods based on the Kullback–Leibler information criterion, which can be used to compare non-nested models. According to the residual sum of squares (RSS), the number of parameters (k) and the sample size (n), AIC and BIC can be used to evaluate IDM and Sigmoid-IDM. The specific formulas of AIC and BIC are as follows:

AIC (Akaike Information Criterion): AIC measures the goodness of fit of the model by the sum of the negative twice log-likelihood and the number of model parameters.
![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/68097e85-944d-46c3-abba-de3fea1ce2a1)

BIC (Bayesian Information Criterion): BIC is based on the Bayesian method, which measures the goodness and complexity of the model by estimating the posterior probability of the model parameters.
![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/92d9e2d8-bc85-44bf-af4d-7403bdccf059)

Our results show that the Sigmoid-IDM model has smaller values on both AIC and BIC, indicating that it has better generalization ability while fitting the Hefei data.

start-up:
 
![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/70f79d64-45c4-401d-a1db-153d30192b42)
![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/f9e3ce04-b8d9-4cc6-8d0a-2f2239d1a5a5)
![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/8f12ca68-b5c8-47db-9366-7635519fbac0)


stop-and-go:

![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/d222a3c1-9f7d-457f-a8fe-0e73e77c6651)
![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/37bfa415-e649-43de-8e8c-968339b3a1ac)

 2.We modified the setting module of the sigmoid branch: we replaced the simple rule of “use IDM if the spacing is larger than the desired spacing, otherwise use Sigmoid-IDM” with a more complex condition that only activates when the spacing is larger than the desired spacing, the speed is lower than a certain threshold and persists for a certain duration, and there is no traffic light. That is
 
 ![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/990fb64e-c404-4a29-8aa1-c54dc78f8eac)

We also simulated and tested the model to demonstrate its improvement in the start-up mode and outflow rate. The results showed that, compared with the original Sigmoid-IDM, the memory effect of the Sigmoid-IDM significantly increased the outflow rate. As shown in Figs A and B, the outflow rate increased considerably under the same input flow.

![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/58899ca6-3668-4984-92bd-5e8ebd237afc)

Fig A. Sigmoid-IDM simulation results with memory effects 

![image](https://github.com/chanstary/Sigmoid-IDM/assets/83267051/065b01d4-7992-439f-b933-afe0d0b6c4de)

Fig B Original Sigmoid-IDM simulation results

