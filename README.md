[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/s0Y_uEY5)
Добрый день, профессор, пришлось изрядно потрудиться за установкой Python, нахождением удобной консоли и скачивания всех модулей и пакетов. Работу делала на Visual Studio Code, поэтому не весь код у меня вышел, пришлось внести некоторые изменения
создала следующий код:
import numpy as np
import pandas as pd
import seaborn as sns
from arch.bootstrap import IIDBootstrap

# Generate a random sample
rng = np.random.default_rng(555555)
x = rng.normal(loc=6, scale=4, size=30)

# Perform a simple bootstrap
bs = IIDBootstrap(x)
results = bs.conf_int(np.mean, 10000)

# Display results # инсталирование пипа PS C:\Users\User\Desktop\Python> python -m pip install pandas numpy seaborn
print("Original Mean:", np.mean(x))
print("Bootstrap Confidence Interval for Mean:", results)


