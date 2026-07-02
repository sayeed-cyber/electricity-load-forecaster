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
