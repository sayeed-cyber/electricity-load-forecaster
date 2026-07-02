## Dataset location

Place the UCI file at:

- `data/household_power_consumption.txt`

## Run

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python main.ipynb
```
or for better debugging run the [this .ipynb file](load_forecasting_simple.ipynb)

The script prints MAE/RMSE for both model and baseline and writes `forecast_results.png`.

## Business Questions

1. **What would you change if you had to forecast for hundreds of thousands of meters at once instead of one?**
   I would not train one model per meter. I would group similar meters and use shared models per segment, then fine-tune only where needed. That scales much better and is easier to maintain

2. **Do you think a model like this is used in practice by utilities, or would something simpler win?**
   A model like this can be used, but in production utilities usually choose the simplest approach that is reliable and easy to operate. If a more complex model gives clear business value, they use it, may be as per roi and the impact is high then they wiil use more complex models with better accuracy

