1. Take input of a list of ETH addresses
2. Record all swaps within SushiSwap and Uniswap originating from the list from 1).
3. Send it to a simple database in the following format:
Timestamp | Address | Action | Token | Amount | TX Hash
{ISO_8601} | 0x.... | Swap | USDC | 100 | 0x.....
This needs to be able to track in real-time subscribing to the necessary event/logs. And it needs to be filtered such that the origination has to be from the list of monitored addresses. (In Uniswap you can do a swap and redirect the token to another address - this is what I want to avoid).
Server UI:
1. A simple page to input additional ETH addresses.
2. A simple tabular page showing the recorded events.
Timestamp | Address | Action | Token | Amount | TX Hash
{ISO_8601} | 0x.... | Swap | USDC | 100 | 0x.....
I will take the next step once I verify the POC and it is working properly based on this specifications. I would need the JS code files to verify on my end once this is completed. I have additional addresses to add on from there for further testing.