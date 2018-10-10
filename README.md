# Node Team Project 1: Texas AirBnB Data

### Import statements below this section

import numpy as np
import pandas as pd
import matplotlib as matplotlib
import matplotlib.pyplot as plt


### Code - Chart 1: Bubble Chart - John




### Code - Chart 2: Adoption - Josh

josh_data = pd.read_csv('Airbnb_Texas_Rentals.csv')
josh_data.head()

# In[57]:
data = josh_data
data = data.fillna('')

# In[58]:
x = data['date_of_listing'].value_counts()[:]
x

# In[59]:
y = data['city'].value_counts()[:]
y

# In[114]:
plt.plot(x, 'ro', markersize=25)
plt.axis([-5, 105, 0, 1000])
plt.subplots_adjust(left=2, bottom=2, right=10, top=4, wspace=2, hspace=2)
matplotlib.rc('xtick', labelsize=20) 
matplotlib.rc('ytick', labelsize=20)
#plt.xticks(range(100)) # add loads of ticks
plt.grid()
plt.gca().margins(x=0)
plt.gcf().canvas.draw()
tl = plt.gca().get_xticklabels()
maxsize = max([t.get_window_extent().width for t in tl])
m = .1 # inch margin
s = maxsize/plt.gcf().dpi*100+2*m
margin = m/plt.gcf().get_size_inches()[0]
plt.gcf().subplots_adjust(left=margin, right=1.-margin)
plt.gcf().set_size_inches(s, plt.gcf().get_size_inches()[1])
plt.gca().invert_xaxis()
plt.show()

# In[157]:
data['city'].value_counts()[:10].plot(kind='barh', color = ['rosybrown','coral','tomato','salmon','sandybrown','navajowhite','mistyrose','bisque','blanchedalmond','linen'])
plt.subplots_adjust(left=2, bottom=2, right=10, top=4, wspace=2, hspace=2)
matplotlib.rc('xtick', labelsize=20) 
matplotlib.rc('ytick', labelsize=20) 
plt.show

# In[67]:
data['date_of_listing'].value_counts()[92:].plot(kind='barh')
plt.subplots_adjust(left=2, bottom=2, right=6, top=4, wspace=2, hspace=2)
matplotlib.rc('xtick', labelsize=20) 
matplotlib.rc('ytick', labelsize=20) 

# In[68]:
data['date_of_listing'].value_counts()[10:20].plot(kind='barh')
plt.subplots_adjust(left=2, bottom=2, right=6, top=4, wspace=2, hspace=2)
matplotlib.rc('xtick', labelsize=20) 
matplotlib.rc('ytick', labelsize=20) 

# In[21]:
# city_index = (data['city'] == 'Houston')

# In[23]:
# city1 = data[city_index]

# In[27]:
# city1['city'].value_counts()[:]
# city1



### Code - Chart 3: Price segments, and then info within each segment - Ashwin



