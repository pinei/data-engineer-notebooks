# Extra

Extra libraries and case studies

- CoinGecko: bitcoin price

## !TODO > Upload Datasets to Kaggle

To upload a new dataset to your Kaggle account using the Kaggle Python API:

```
pip install kaggle
```

Make sure you have a Kaggle API token. If you don't have one, you can generate it from your Kaggle account.

- Go to your Kaggle account settings
- Scroll down to the "API" section
- Click on "Create New API Token"

This will download a JSON file containing your API credentials. Place the downloaded JSON file in the appropriate directory.

By default, the Kaggle API expects the file to be in the .kaggle directory in your user's home directory.

```
import kaggle

# Set the file path of the dataset you want to upload
file_path = '/path/to/your/dataset.csv'

# Initialize the Kaggle API
kaggle.api.authenticate()

# Create a new dataset
dataset_metadata = kaggle.api.dataset_create_new(dataset_name='Your Dataset Name',
                                                 title='Your Dataset Title',
                                                 subtitle='Your Dataset Subtitle',
                                                 description='Your Dataset Description')

# Upload the dataset file
kaggle.api.dataset_upload_file(dataset_metadata['id'], file_path)
```

### References

- ChatGPT
- [Kaggle Python API](https://www.kaggle.com/code/donkeys/kaggle-python-api/)