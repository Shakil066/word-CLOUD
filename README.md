# word-CLOUD
#Text data analysis
from wordcloud import WordCloud
import pandas as pd
import matplotlib.pyplot as plt
df=pd.read_csv("games.csv")
df.head()
text = " ".join(cat.split()[1] for cat in df.category)
word_cloud = WordCloud(collocations = False, background_color = 'white').generate(text)
plt.imshow(word_cloud, interpolation='bilinear')
plt.axis("off")
plt.show()
