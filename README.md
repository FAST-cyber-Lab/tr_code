# Clone the repository.<br>
git clone https://github.com/FAST-cyber-Lab/tr_code.git
cd codevulplus

### Create a virtual environment (recommended).<br>
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

### Install dependencies.<br>
pip install -r requirements.txt

## Download Pretrained Models.<br>
python scripts/download_models.py

## Run demo.<br>
python simplerun.py


## Generate Embeddings from Your Own Code.<br>
python infer.py --dataset your_dataset.csv --model_path pretrained/pretrained.pt --output your_embeddings.csv

## Make Vulnerability Predictions.<br>
python predict.py --embeddings your_embeddings.csv

## To train the model on your own dataset.<br>
python train.py --dataset your_dataset.csv --save_path models/your_model.pt --batch_size 16 --epochs 10
