# hello-solana

## Running the tests
`anchor test`

This will build, deploy, and test programs against a specific cluster.

## Configure devnet cluster
`solana config set --url devnet`
## Make sure you are on the devnet cluster
`solana config get`
## Build the program
`anchor build`
## Generate a new program id
By default, Anchor generated a program id for local development. We need to generate a program id before we deploy to devnet

`solana address -k target/deploy/my_solana_program-keypair.json`
## Update program id in Anchor.toml and lib.rs
Now that you have the program id, open the Anchor.toml file and do the following:
- Update [programs.localnet] to [programs.devnet].
- Update the program id set in my_solana_program with the new program id.
- Update the cluster to cluster = "devnet".`
## Build the program one more time
`anchor build`
## Deploy to devnet
`anchor deploy`
# good ref
https://www.becomebetterprogrammer.com/create-solana-smart-contract/
