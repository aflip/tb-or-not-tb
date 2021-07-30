This is a Deep learning powedred app that detects TB from chest X rays.


Made with [Fast.ai](https://github.com/fastai/fastai) and trained on the the [Montgomery and Shenzhen TB datasets](https://lhncbc.nlm.nih.gov/LHC-publications/pubs/TuberculosisChestXrayImageDataSets.html) and tested on the [Jaypee institute TB Dataset](https://sourceforge.net/projects/tbxpredict/) [5]

The app is strictly not for diagnosis or treatment or making medical deicions as it has not undergone any clinical testing yet.

[The working app can be found here, served with voila and binder](https://hub.gke2.mybinder.org/user/aflip-tbornottb-piipw70u/voila/render/TB_or_not_TB.ipynb?token=JdX_LwudQFaa6GOuNneIuw) (This is down, for now)


## How reliable is the Chest X-ray (CXR)

In practice, the CXR is used widely to make a confirmation of TB. It is also considered to be very sensitive for TB. Probably more sensitive than just a sputum test. However, the inter-operator variablity in CXR reading is a big problem in TB. [3] Screenshots are from Toman TB  [4]

![Observer error](/img/observer_error.png)
![Inter operator agreement](/img/inter_operator_agreement.png)
![Disagreement specification](/img/IUAT_disagreement_index.png)

in summary, the chapter on CXR reliability says:

![X-rays summary](/img/in_summary.png)


Multiple studies have shown that DL models provide consistant and reliable TB diagnosis from CXRs [6][7]

I think removing the inter-operator bias, and Dl models that provide more than just lables with confidence, but also include localization, heaptmaps or boundary boxes will go a long way in improving the diagnosis making process of TB.



## Roadmap:

1. Explainable predictions (Heatmap or bounding boxes)
2. Better models
3. Model Zoo



### References:


[1] @misc{howard2018fastai,
  title={fastai},
  author={Howard, Jeremy and others},
  year={2018},
  publisher={GitHub},
  howpublished={\url{https://github.com/fastai/fastai}},
}

[2] Jaeger, S., Candemir, S., Antani, S., Wáng, Y. X., Lu, P. X., & Thoma, G. (2014). Two public chest X-ray datasets for computer-aided screening of pulmonary diseases. Quantitative imaging in medicine and surgery, 4(6), 475–477. https://doi.org/10.3978/j.issn.2223-4292.2014.11.20

[3] World Health Organization. (‎2016)‎. Chest radiography in tuberculosis detection: summary of current WHO recommendations and guidance on programmatic approaches. World Health Organization. https://apps.who.int/iris/handle/10665/252424

[4] Toman, K. (2004). Toman's Tuberculosis: case detection, treatment, and monitoring: questions and answers. World Health Organization.

[5]  Chauhan A, Chauhan D, Rout C (2014) Role of Gist and PHOG Features in Computer-Aided Diagnosis of Tuberculosis without Segmentation. PLoS ONE 9(11): e112980. https://doi.org/10.1371/journal.pone.0112980

[6] Harris, M., Qi, A., Jeagal, L., Torabi, N., Menzies, D., Korobitsyn, A., Pai, M., Nathavitharana, R. R., & Ahmad Khan, F. (2019). A systematic review of the diagnostic accuracy of artificial intelligence-based computer programs to analyze chest x-rays for pulmonary tuberculosis. PloS one, 14(9), e0221339. https://doi.org/10.1371/journal.pone.0221339

[7] Qin, Z. Z., Sander, M. S., Rai, B., Titahong, C. N., Sudrungrot, S., Laah, S. N., ... & Creswell, J. (2019). Using artificial intelligence to read chest radiographs for tuberculosis detection: A multi-site evaluation of the diagnostic accuracy of three deep learning systems. Scientific reports, 9(1), 1-10.
