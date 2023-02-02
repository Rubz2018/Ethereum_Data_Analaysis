# Ethereum Data Analysis dataset selection and maintenance guidelines:
 - Time period - From 2015 to data. Full up to date blockchain data.
 - The dataset needs to be authentic and reliable to do research.
 -  Needs to be properly pre-processed.
 -   

## Tagetted Attributes:
The following attributes are taken from the kaggle dataset uaing bigquery(https://www.kaggle.com/datasets/bigquery/ethereum-blockchain).The attributes needs to be assigned as lowercase in the dataframe table. We might have to use GitHub repo(https://github.com/medvedev1088/ethereum-etl) to download the ethereum on chain data by installing Geth and downloading it locally.  
- Blocks    
The Ethereum blockchain is composed of a series of blocks. This table contains a set of all blocks in the blockchain and their attributes.
            |- timestamp
            |- block Number
            |- block Hash
            |- previous BlockHash
            |- nonce (For Ethereum it is the unique identifier)
            |- transactions_root(Merlel Root?)
            |- state_root
            |- Receipts Root
            |- miner
            |- difficulty
            |- total difficulty
            |- block_size(in kilobyte)
            |- gas_limit
            |- gas_used
            |- transaction_count
- Contracts 
Some transactions create smart contracts from their input bytes, and this smart contract is stored at a particular 20-byte address.
            |- contract_address
            |- is_erc20
            |- is_erc721
            |- block_timestamp
            |- block_number
            |- block_hash
- Token Transafer
The most popular type of transaction on the Ethereum blockchain invokes a contract of type ERC20 to perform a transfer operation, moving some number of tokens from one 20-byte address to another 20-byte address.
The following attributes contain the subset of those transactions and has further processed and denormalized the data to make it easier to consume for analysis of token transfer events.
                  |- token_address
                  |- from_address
                  |- to_address
                  |- value(in wei)
                  |- transaction_hash
                  |- block_timestamp
                  |- block_number
                  |- block_hash
- tokens: 
Token data.
                |- address
                |- token_name
                |- decimal
                |- total_supply
                |- block_timestamp
                |- block_number
                |- block_hash
-  traces:
    Need to get clear ideas about what traces represent.

-  transactions: 
                |- hash
                |- nonce
                |- transaction_index
                |- from_address
                |- to_address
                |- value(in wei)
                |- gas
                |- gas_price
                |- input
                |- receipt_cumulative_gas_used
                |- receipt_gas_used
                |- receipt_contract_address
                |- receipt_root
                |- receipt_status
                |- block_timestamp
                |- block_number
                |- block_hash



                


    