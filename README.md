# Improving Reinforcement Learning Trading Model with CDC Trailing Stop Strategy

This project was undertaken as part of my Master's degree independent study at NIDA University. 
In my view, teaching a reinforcement learning agent to learn how to trade independently can be very challenging. 
I discovered that existing trading strategies can serve as helpful guidelines for traders in making decisions about when to buy or sell.
Therefore, I attempted to guide my RL agent using an existing strategy.

Specifically, I chose the 'CDC ATR Trailing Stop' strategy, which is easy to use. 
The strategy involves a green and red indicator that signals when to buy or sell. 
The original strategy suggests buying when the color changes from red to green, holding the buy position as long as the color remains green, 
and closing the position when it turns red. Conversely, the strategy for a sell position is the opposite. 
I considered this indicator as a trend indicator, where trading on the buy side only when the indicator is green and trading on the sell side only when it is red. 
I implemented this concept as a penalty component in the reward function of my RL model. 
If the model trades in the direction opposite to the indicator's color, it receives a penalty. 
With this approach, I expected the agent to learn to trade following the strategies, 
while also being courageous enough to trade on the opposite side at times if the return is worth receiving a penalty.

The results showed that adding this penalty component had a significant impact on model performance. 
The model was able to generate higher profits compared to both the original strategy and the RL model without this component.



