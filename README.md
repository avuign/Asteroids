# 1) Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# 2) Make `brew` available in this Terminal session (Apple Silicon Macs)
eval "$(/opt/homebrew/bin/brew shellenv)"

# 3) Install Git + Python 3
brew install git python

# 4) Download your game
git clone https://github.com/avuign/Asteroids.git
cd Asteroids

# 5) Create + activate a virtual environment
python3 -m venv venv
source venv/bin/activate

# 6) Install dependencies + run
python -m pip install -U pip
python -m pip install pygame
python3 main.py
