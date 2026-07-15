# iRT Coupled PINN

## Initial Conditions

The PINN declares the initial conditions for the 5 vairables below. These values were developed with the idea that one single dose was administered previously, but i am working to develop a fractionation schedule, which would change the initial conditions of the damaged tumors, irradiated tumors, and the lymphocytes.

<img width="411" height="135" alt="Screenshot 2026-07-15 at 12 05 14 PM" src="https://github.com/user-attachments/assets/064a29dc-f61f-42c5-a143-0f1847e808ee" />

## Parameters

These parameters are used exclusively in the loss function of the PINN. Separately, the constant, L_scale = 1e9, is used to scale the lymphocyte count and the other lymphocyte parameters because the scaling keeps the network's output weights in a trainable range and prevents the L residualfrom dominating the total loss. Rate constants. such as lamda and delta_L are left unscaled, since they multiply L linearly and scale correctly on their own.

<img width="504" height="346" alt="image" src="https://github.com/user-attachments/assets/9ee15fe5-78bc-44b5-8bf1-11d33bd99b8c" />

