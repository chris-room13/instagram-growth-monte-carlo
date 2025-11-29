📈 Instagram Growth Monte Carlo Simulation

This mini project estimates how many days it will take to reach 100,000 Instagram followers using a Monte Carlo simulation based on your last 10 days of real growth data.

It uses simple bootstrapping:
each simulated day randomly samples one of your recent daily growth values and sums them until the target follower count is reached.
Running thousands of simulations provides an estimated distribution of outcomes.

🚀 Features

Run a Monte Carlo simulation to estimate the time needed to hit 100k followers

Use your real last 10 days of growth as the distribution

Visualize the distribution with histograms

Implemented entirely in a VS Code Jupyter Notebook

Lightweight project using uv, numpy, and matplotlib

📁 Project Structure
instagram-growth-monte-carlo/
│
├── monte-carlo.ipynb     # Notebook with simulation code
├── pyproject.toml         # Package/environment config (uv)
├── README.md              # Documentation
├── LICENSE                # MIT license
└── .gitignore             # Ignores virtual envs, cache files, etc.

🛠️ Installation & Setup

Clone the repository:

git clone https://github.com/<your-username>/instagram-growth-monte-carlo.git


Enter the project folder:

cd instagram-growth-monte-carlo


Install dependencies using uv:

uv sync


Open the Notebook in VS Code and select the project’s .venv as the Python kernel.

📊 How It Works

Inside the notebook:

Define your real growth data:

current_followers = 5000
last_10_days_growth = [120, 95, 150, 130, 110, 160, 90, 140, 100, 125]


Run the Monte Carlo simulation:

stats = estimate_days_to_target(last_10_days_growth, current_followers)
stats


Visualize the distribution (optional):

plt.hist(results, bins=50)

📬 Contributing

This is a lightweight mini project — contributions welcome for:

Better visualization

Parametrized notebook

Web dashboard (Streamlit)

Instagram API integration