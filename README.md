
# Seth Notes for Dojo Starter

## Steps for Development and Deployment

1. **Import Required Models**  
   Ensure you import all necessary models in the parent module of your function.

2. **Compile the Contract**  
   After making changes, compile the contract by running: `sozo build`

3. **Migrate and Deploy**  
   Update and deploy the contract using:  `sozo migrate`

4. **Start the Local Environment**  
   Run the local development environment with: `katana --dev`

5. **Execute Actions**  
   Execute your new action using: `sozo execute actions {function_name} -c {params}`
   
   - For `felt252` data types, format strings as `sstr:"string"`.

   - **Example**:  
     
     `sozo execute actions update_username -c 1,sstr:"misty" --wait --receipt`

     **Note**: Separate parameters with commas **without spaces**.

6. **Key Arguments for Execution**  
   - `--wait`: Waits for the transaction to complete before returning the transaction hash.  
   - `--receipt`: Provides a receipt of the transaction.

7. **Fetching Data**  
   To retrieve data from a deployed contract, use: `sozo model get {model_name} {key}`


    - **Example**:  
     
     `sozo model get Player 1`

