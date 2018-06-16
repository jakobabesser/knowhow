# Matplotlib #

* Remove ticks
``` python
pl.xticks([], [])
pl.yticks([], [])
```
* Change tick sizes
``` python
ax.set_xticklabels(ax.get_xticklabels(), rotation=90)
for tick in ax.yaxis.get_major_ticks():
    tick.label.set_fontsize(self.fontsize)
```
* Tighten layout
  * ``` pl.tight_layout() ```
* Flip y-axis (useful for plotting spectrograms)
  * ```pl.gca().invert_yaxis()```
* Plot spectrogram
  * ```pl.imshow(spec, interpolation=”nearest”, aspect=”auto”) ```  
* Legend
  * ```pl.legend(loc=0)```

* Multiclass scatter plot

``` python
colors = ('c', 'm', 'r', 'g', 'b', 'k', 'y') * 3
markers = ('o', 's', 'd', 'o', '<', '>', '^', 'p') * 3
for cid in np.arange(num_classes):
    idx = class_id == cid
    plt.scatter(mat[idx, 0], mat[idx, 1], label=class_label[cid], c=colors[cid], marker=markers[cid], alpha= .2 if cid == 0 else .8, s=25)
plt.gca().legend(loc=0, fontsize=8, scatterpoints=1)

```


# Seaborn  / Pandas

* Scatter plot
```python
df = pn.DataFrame({'x': x,
                   'y': y})
        df.plot(kind='scatter',
                x='x',
                y='y')
```

* scatter plot with linear regression line
``` python
df = pn.DataFrame({'x': x,
                   'y': y})
sns.set_style("whitegrid")
g = sns.lmplot(x='x',
               y='y',
               markers="o",
               data=df,
               ci=None,
               # palette="Blues_d",
               size=3.5,
               scatter_kws={"s": 10, "alpha": 1})
g.set_xticklabels(rotation=60)
g.set(ylim=(0, 50))
```     

* density plot
```python
pl.figure()
g = pn.Series(array_to_plot).plot.kde(x='x label text',
                                      linestyle=l'-',
                                      label='my label')
g.set(xlim=(-50, 50))
g.set(xlabel='my x label')
```
