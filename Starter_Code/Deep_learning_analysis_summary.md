# Deep Learning - LSTM Stock Predictor using RNN
## By Franklin Vaca
<p>Use of Deep Learning techniques: LSTM - Long short-term memory - RNN Recurrent Neural Networks and FNG (Crypto and Fear) Index to predict closing prices in Bitcoin.
The results presented here were extracted from two jupyter notebooks: lstm_stock_predictor_fng.ipynb and lstm_stock_predictor_closing.ipynb located in the Starter_files folder of this repository.</p>
<p></p>

## **Considerations for the analysis:**
<p>Two models were built using deep learning recurrent neural networks to model bitcoin closing prices. The first model uses FNG indicators to predict the closing price while the second model uses a window of closing prices to predict the nth closing price. The window sizes and batch sizes used on both models are:</p>
<p>- Four window sizes (10-day, 5-day, 3-day and 2-day) 
</p>
<p>- Four batch sizes (90, 50, 10 and 1) 
</p>
<p>These variations in window and batch size were used in both models to evaluate the window and batch size that had the smaller loss.</p>
<p>The batch size:1 was selected for the predictions because it offered the smaller loss when comparing the FNG and the closing models side by side.</p>
<p></p>
Date: 10/08/2021

## **Model Comparison**
### **1. Which model has a lower loss?**<br>
><p>Overall, the closing-prices model had lower losses compared to the FNG model. The closing-prices model using a 2-day window had the lowest loss at: 0.0495. The different loss values by model and window are:  </p><br>

*Loss of the FNG models using different time-windows* 

![image](Analysis_graphs/FNG_model_loss_comparison.PNG)
<p></p><br>


*Loss of the Closing-price models using different time-windows* 

![image](Analysis_graphs/Closing_prices_loss_comparison.PNG)

<p></p><br>


### **2. Which model tracks the actual values better over time?**<br>
><p>The closing-prices model seems to track the actual closing values of Bitcoin better. The plots below show that the closing-prices model makes a better job at mimicking the behavior of Bitcoin prices overtime. The 2-day closing-prices model has the lowest loss and could predict bitcoin closing prices better than the rest of the models analyzed.</p><br>
<p></p>

## *Closing-prices Model Plots:* 
![image](Analysis_graphs/Closing_prices_plot_2d.PNG)
![image](Analysis_graphs/Closing_prices_plot_3d.PNG)
![image](Analysis_graphs/Closing_prices_plot_5d.PNG)
![image](Analysis_graphs/Closing_prices_plot_10d.PNG)

<p></p><br>

## *Fear and Greed (FNG) Model Plots:* 
![image](Analysis_graphs/FNG_model_plot_2d.PNG)
![image](Analysis_graphs/FNG_model_plot_3d.PNG)
![image](Analysis_graphs/FNG_model_plot_5d.PNG)
![image](Analysis_graphs/FNG_model_plot_10d.PNG)

<p></p><br>

><p>The Fear and Greed index model seems to capture the downward trends of Bitcoin prices but does not capture price increases.</p><br>

<p></p><br>

### **3. Which window size works best for the model?**<br>
><p> The 2-day window in the closing-price model had the lowest loss at: 0.0495. Among the FNG model, the use of a 3-day window had performed slightly better than the rest, having the smallest loss (0.1566) across the FNG models.</p>
><p>Overall, the closing-price model with a 2-day window was the better predictor for Bitcoin closing prices.
</p><br>

*Loss of the Closing-price models using different time-windows* 

![image](Analysis_graphs/Closing_prices_loss_comparison.PNG)

<p></p><br>
*Loss of the FNG models using different time-windows* 

![image](Analysis_graphs/FNG_model_loss_comparison.PNG)

<p></p><br>


