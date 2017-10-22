# TODOS

## Technical

### [TODO] - Write a truffle migration that successfully deploys the main contracts

Problems:

- There is some kind of cyclic import problem to get fixed
- Doing the whole thing seems to be requiring too much gas. For that, we have split down the deployment steps (see below). But it seems the MinnieBank deployment it still too expensive.

Migration steps:

- Create MinnieGovernance
- Launch `createProposalValidator`
- Launch `createMinnieBank`
- Launch `createGovernanceProxy`

### [TODO] - Write some tests

- Create TestProposal
- Instantiate ProposalValidator
- Launch `ProposalValidator.vote(test proposal addr, true)`
- Launch `MinnieGovernance.executeProposal(test proposal addr)`

## Security

### [TODO] - Make sure the `onlyowner` decorator is well properly in use

## Documentation

### [TODO] - Explain in more detail what is the interface of MinnieBank and of ProposalValidator

### [TODO] - Write jsdoc for important methods

## Features

### [TODO] - Prevent a proposal to get executed twice.

### [TODO] - Enhance the quorum calculation in the ProposalValidator

Use proportion.

### [TODO] - Make MinnieBank ERC20 compliant
