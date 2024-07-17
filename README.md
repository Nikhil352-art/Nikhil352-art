import pandas as pd
import plotly.express as px
import plotly.graph_objects as go
from dash import Dash, dcc, html

# Sample data
data = {
    'date': pd.date_range(start='2023-01-01', periods=30, freq='D'),
    'likes': [50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 150, 160, 170, 180, 190, 200, 210, 220, 230, 240, 250, 260, 270, 280, 290, 300, 310, 320, 330, 340],
    'comments': [5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34]
}

df = pd.DataFrame(data)

# Initialize the Dash app
app = Dash(__name__)

# Define the layout
app.layout = html.Div([
    html.H1("Social Media Analytics Dashboard"),
    dcc.Graph(
        id='likes-graph',
        figure=px.line(df, x='date', y='likes', title='Daily Likes')
    ),
    dcc.Graph(
        id='comments-graph',
        figure=px.bar(df, x='date', y='comments', title='Daily Comments')
    )
])

# Run the app
if __name__ == '__main__':
    app.run_server(debug=True)
- 👋 Hi, I’m @Nikhil352-art
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Nikhil352-art/Nikhil352-art is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
