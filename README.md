# Music Genre Popularity Over Time: Sampling and Survey Analysis

## 1. Introduction

The evolution of popular music genres reflects changes in cultural trends, technological innovation, and consumer behavior. Over the last few decades, the music industry has experienced dramatic growth in digital distribution and streaming, which has allowed certain genres to rise rapidly in visibility. This study analyzes a dataset of top-charting songs with genre, year, and other metadata, with the goal of quantifying trends and evaluating sampling strategies in representing the population distribution of genres.

Key objectives:
Normalize diverse genre labels into broad, meaningful categories.
Examine temporal patterns in song counts and genre composition.
Compare simple random sampling (SRS) and stratified sampling for representativeness.
Visualize trends and interpret them in a clear, accessible manner.

## 2. Methods

2.1 Data Preparation

The dataset contained song-level metadata including year, genre, artist, and popularity metrics. Genres were normalized into major categories (Pop, Hip-Hop/Rap, Rock/Metal, Country, Latin, R&B/Soul, Electronic, Indie/Folk, K-Pop/K-Rap, Classical, Afrobeats) and a catch-all "Other" category. Very small categories (less than 2% of total) were reassigned to "Other" to reduce sparsity and simplify analysis.


### 2.2 Sampling Techniques

- **Simple Random Sampling (SRS):** 200 songs randomly selected, representing a typical survey approach.
- **Stratified Sampling:** proportional sampling within each genre group to preserve population proportions, particularly for smaller genres.

	
## 2.3 Data Analysis and Visualization

- **Temporal trends**: line and area charts to capture yearly changes.
- **Distributional comparisons**: bar charts to evaluate SRS vs stratified representation.
- **Decade-level comparisons**: stacked bar charts to identify long-term shifts.
- Tools: R packages dplyr, ggplot2, and forcats.

## 3. Results

### 3.1 Genre Distribution Across Population

After normalization, Pop (42.7%) and Hip-Hop/Rap (19%) dominate the population, while most other genres constitute smaller fractions. The "Other" category, representing songs that could not be clearly assigned, was reduced, indicating successful consolidation of minor genres.

Observation: The dataset is heavily skewed toward modern mainstream genres, which may reflect charting trends or dataset bias toward contemporary popular music.


### 3.2 Music Popularity Over Time

Figure 1: Music Popularity Over Time
Strong acceleration in song counts is observed after 2015, indicating higher volume of recorded or charting songs in recent years.
Pop dominates late-year entries, followed by Hip-Hop/Rap, suggesting these genres are driving modern music production.
Other genres remain relatively flat, with occasional spikes.
Interpretation:
This figure indicates a strong upward trend in the number of songs represented in recent years, with Pop showing the steepest increase and Hip-Hop/Rap also rising substantially. The pattern suggests that contemporary entries in the dataset are heavily concentrated in a few dominant genres.

![](/Plots/Music%20Popularity%20Over%20Time.png)


### 3.3 Population vs Simple Random Sample

Figure 2: Population vs SRS
SRS captures the broad population distribution, preserving relative dominance of major genres.
Deviations exist for medium-sized categories (e.g., Hip-Hop/Rap slightly overrepresented, Pop slightly underrepresented).
Small or rare genres are less consistently represented due to random sampling fluctuation.
Interpretation:
The SRS distribution broadly follows the population distribution, preserving the dominant ranking of genres. However, visible differences for specific groups demonstrate expected random sampling variability. For smaller genres, SRS may fail to accurately capture representation.

![](/Plots/Population%20vs%20SRS.png)


### 3.4 Genre Proportion Trends Over Time

Figure 3: Genre Proportion Over Time
Early years show a diverse mix with notable Rock/Metal presence.
From the 2000s onward, Pop rose rapidly, accompanied by growth in Hip-Hop/Rap.
Other minor genres fluctuate without sustained growth.
Observation: The stacked area plot visually exceeds 100% in some periods due to overlapping counts, so interpretations are qualitative.
Interpretation:
The stacked trend illustrates a long-run compositional change in genre mix, with stronger modern prominence of Pop and Hip-Hop/Rap. Because the stacked total appears inconsistent in parts of the figure, this chart is best used for directional interpretation rather than exact quantitative inference.

![](/Plots/Genre%20Proportion.png)

### 3.5 SRS vs Stratified Sampling

Figure 4: SRS vs Stratified Sampling
Stratified sampling provides a more stable representation across all genre groups.
SRS exhibits larger swings in medium and small categories due to random variability.
Interpretation:
Compared with SRS, the stratified sample maintains genre representation more consistently across categories. Stratified sampling is therefore advantageous when the goal is proportional representation of all groups, especially when class sizes are uneven.

![](/Plots/SRS%20vs%20Stratified.png)

### 3.6 Decade-Level Genre Shifts

Figure 5: Genres Per Decade
1980s-1990s: Rock/Metal shows stronger relative presence.
2000s onward: Pop emerges as the dominant genre, with Hip-Hop/Rap growing steadily in later decades.
Smaller genres remain present but do not show sustained growth trends.
Interpretation:
The decade comparison highlights a structural shift in genre leadership: Rock/Metal is comparatively stronger in earlier decades, while Pop and Hip-Hop/Rap dominate the 21st century. The pattern is consistent with changing mainstream listening trends over time.

![](/Plots/Genres%20Per%20Decade.png)

## 4. Discussion
**Time-Based Concentration**: The dataset demonstrates a strong temporal concentration of songs in the modern era, with accelerated production and charting after 2015.

**Dominant Genres**: Pop and Hip-Hop/Rap emerge as the primary growth drivers, while other genres maintain minor presence.

**Sampling Implications:**
SRS adequately reflects dominant genres but introduces variability in small or medium categories.
Stratified sampling better preserves proportional representation, supporting its use in survey studies or analyses requiring stable estimates across groups.

**Genre Evolution:**
Historical dominance of Rock/Metal gradually shifts to modern Pop and Hip-Hop/Rap, indicating cultural and industry-wide changes in listener preferences.
Minor genres, although individually sparse, collectively contribute to diversity and are captured in the "Other" category.

## 5. Conclusion
Across all figures, the central pattern is a time-based genre shift and concentration: recent years contain many more songs and are dominated by Pop, with Hip-Hop/Rap as the second strongest growth genre. Sampling comparisons show that while simple random sampling captures broad structure, stratified sampling provides a more stable representation. Decade-level results reinforce the long-run transition from earlier Rock/Metal prominence to modern Pop and Hip-Hop/Rap dominance.


## 6. References

Kaggle: Spotify Songs and Artists Dataset | Audio Features:
https://www.kaggle.com/datasets/glowstudygram/spotify-songs-and-artists-dataset
