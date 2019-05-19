# Qusestions of state representation learning (code: srl-zoo)
###train.py

 what's dae?
```
dae: Denoising Autoencoder
```

## losses.py
```
function kullbackLeiblerLoss(..) has the parameter beta for adapting the disentangling of beta-VAE implementation
```

## learner.py
```
DataLoader.createTestMinibatchList(..)
```

# How to use the trained srl model?
### evaluation and plotting
1.To view the learned state and play with the latent space of a trained model, you may use: 
```
python -m evaluation.enjoy_latent --log-dir logs/nameOfTheDataset/nameOfTheModel
```
2.You can also plot ground truth states with:
```
python -m plotting.representation_plot --data-folder path/to/datasetFolder/
```
Here, an issue was encountered, as shown in 
![](/home/birl_wu/papers_notes_remarkable/images/error_representation_plot.png) 
and the plotted figure as 
![](/home/birl_wu/papers_notes_remarkable/images/error_representation_plot_2.png) 
This issue can be solved by adding the following codes before the fig.tight_layout  in the **representation_plot.py** file.
![](/home/birl_wu/papers_notes_remarkable/images/2019-05-19_17-01.png) 
Cosequently, the result shown as
![](/home/birl_wu/papers_notes_remarkable/images/2019-05-19_17-06.png) 