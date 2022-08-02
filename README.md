# Chemotaxis-Dashboard

Welcome to the Chemotaxis-Dashboard repository on GitHub!

Migration of neutrophils to a nidus of infection is a critical component of the host innate immune response; defects in neutrophil chemotaxis can have a severe impact on immune function. Timelapse videos of neutrophil chemotaxis in response to a chemoattractant can be a valuable tool for diagnosing rare defects, but manual collection of quantitative data from these videos can be tedious and time-consuming. We have developed an AI-based workflow to automatically segment and track the paths of individual migrating cells and provide some measures of cell shape.

The chemotaxis dashboard facilitates exploration of summary statistics for each cell (cell velocity over time and direction of movement) and for each sample (average velocity over time, average direction of movement, and the proportion of cells successfully migrating across the area of observation). Cells from different samples can be clustered, compared and contrasted based on the distribution of these summary statistics (e.g. cells obtained from healthy donors vs patients or cells responding to different chemoattractants).

The rest of this README contains lower-level notes and information on the repository itself. For additional information, checkout [this vignette](https://abcsfrederick.github.io/Chemotaxis-Dashboard/poster.html), or you can try out the shiny app with some simulated data on [shinyapps.io](https://mckalliprn.shinyapps.io/demo_app/?_ga=2.247871367.1296701277.1659379204-1106696516.1659379204).

## Utilities

We have a number of R scripts included in the `utils/` directory, and we are working on documenting them here. Check back soon for additional details.

* Preprocessing raw tracks and calculation of summary statistics
  * `preprocess.R` 
  * `one_experiment.R`
* Preprocess data in batches on our HPC cluster
  * `make_swarm.R`
  * `mergeData.R`
* Identifying specific images to use for each cell for cell shape analysis
  * `findGoodFrames.R`
* Clustering of cell tracks
  * `clustering_code.R`
