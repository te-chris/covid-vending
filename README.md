# Covid Vend - The Vending Machine for all your COVID-19 essentials.
This is a command-line vending machine to supply you with all the lockdown essentials you need.
## Installation and setup
Ensure you have `ruby` and `sqlite3` installed, then run:
1. Run `bundle install` to install any gems.
2. Run `covid-vend init` to setup the machine
## Usage
`bin/covid-vend COMMAND ARGS`
### Available Commands:
- `init` - This creates a `sqlite3` db and fills the machine with stock and change
- `update_item ITEM_NAME QTY` - This command allows you to add new items to the machine and update the available quantity
- `purchase_item ITEM_NAME QTY` - This command allows you to purchase items. It will ask you to insert an amount of change, then will return your precious stocks to you, for easy depositing in your bunker. If you haven't put in enough money, your change is returned to you. If the machine doesn't have enough money, your change is returned to you
- `update_change CHANGE_LIST` - This command allows you increment the availabe change in the machine. It expects a comma separated list of integer values in the format `1p,2p,5p,10p,20p,50p,£1,£2`. Any values ommitted will cause the update to fail.
- `available_items` - This lists current stock levels
## Development
Missing something? Really wish the output was ASCII colour formatter? Modify to your heart's content. The core business logic lives in `/lib`.  The main entry point to the vending machine is `covid_vend.rb

Tests live in `/spec`. Run these with `bundle exec rspec spec`

## Next Steps

