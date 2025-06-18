# Gold Mining Detection in Prey Lang Wildlife Sanctuary Using Sentinel-1 SAR

# Summary
This project focuses on detecting the presence of gold mining activities deep within the Prey Lang Wildlife Sanctuary. The goal was to uncover the environmental scars left by gold mining operations and create visualizations that narrate the story of Prey Lang’s transformation.

# Approach

1. Area of Interest Selection:

The AOI is located in central-southern Prey Lang. This location was chosen because it lies outside the official boundaries of established mining concessions but still shows signs of potential mining activities (Fig 2). 

Changing the only the coordinates of the AOI allows the code to be transferable to any forested area worldwide.

2. Data Collection:

  * Sentinel-2: These images were used to create a timeseries of the AOI, providing visual evidence of land cover changes (Fig 1).
      * Created cloud free images before and after the opening of the mine for a splitmap.
      * Created a GIF animation showing cloud free composites of the AOI (Fig 1).

  * Sentinel-1 SAR: I identifed the images suitable for the construction of a time series of preprocessed datasets.
      * These images, with a resolution of 5 metres, allow for near real-time monitoring and can penetrate through clouds, making them suitable for rainforest environments. SAR imagery is effective for detecting changes in soil structure and moisture content, which are key indicators of gold mining activity. This is due to the use of water in extraction processes, the accumulation of chemical pools, and the significant land deformation that are typically a consequence of the operations.

3. Data Analysis:

Using the methodology outlined in Monitoring Gold Mining Activity Using SAR (Villa et al., 2024), I generated alerts of deforestation that fit within the peramiters of hydraulic gold mining.
  *  I ran a change detection analysis based on a statistical analysis of the Sentinel-1 images.
  *  I filtered the results with maximum area patches and information of forest/non-forest and water bodies.


![AOIyear](https://github.com/user-attachments/assets/4dd4bd8b-9b27-42b2-ae3e-55470d0f5e5a)

Figure 1: Timelapse of Sentinel 2 images showing annual changes in the AOI from 2018-2025



![Screenshot 2025-04-01 at 20 07 59](https://github.com/user-attachments/assets/9f5058dd-33b5-41aa-ad71-336f81a736b2)

Figure 2: Known Mining concessions cover 42% of the Prey Lang Wildlife Sanctuary. 250000 hactares of the largest lowland rainforest in mainland Southeast Asia, Home to 80% of the native tree species an many threatened species of plants and animals. Mining companies publications are the main source of data. Government data is sparce, which is cause for concern. 


# Results

Mining operations in the region are well-documented by journalists, highlighting the environmental and social pressures, and revealing links between concession owners, government officials, and potential corruption. A mining concession database confirms the prevalence of gold mining in the southern part of Prey Lang, and when overlaid on a map (FIG 2), it shows that the AOI straddles the border of an established gold mining concession.

The results indicate that hydraulic mining activity was detected in the western pit through 2024 (FIG 4). This activity may be linked to the 28% surge in gold price during that year. Furthermore, smaller artisanal operations may be responsible for the detections observed outside the main pits (FIG 3). Further on-the-ground research is needed to corroborate these findings and refine the environmental filters in post-processing for more accurate results.
 
Alternatively, the results suggest an absence of hydraulic gold mining. Figure 3 displays hotspots in the mining pits over the three years they have been operational. These results are most likely due to excavatioins that do not use water, concluding that, while these mines are causing similar environmental destruction and providing access for illegal loggers, they may be less environmentally damaging compared to other methods of mineral extraction. Their place in a protected area, although, is contentious.

I am currently applying this methodology to a known gold mining site to the west of the AOI, within Prey Lang, to determine the optimal thresholds for the filters to be applied during processing of the Sentinel-1 timeseries mosaic. 

![Screenshot 2025-04-01 at 20 21 32](https://github.com/user-attachments/assets/685b3fcb-c285-46f9-a9ac-28fab586a2ca)

Figure 3: SAR change detection results after applying the Q test algorythm. The colours correspond to the date of detection.



![Screenshot 2025-04-01 at 20 21 48](https://github.com/user-attachments/assets/3f84a757-6a21-4ab1-b4a0-a1ee07e83848)

Figure 4: Results after filtering to eliminate false positives. 


# The problem of concessions

Forest loss in Prey Lang is accelerating, particularly in the south. The wildlife sanctuary was designated as protected in 2016. Despite the sanctuary’s legal protection, deforestation continues due to mining activities and other resource extractions. Research has shown that Economic Land Concessions (ELCs) are significant drivers of deforestation in Cambodia (Pauly et al., 2022), and mining operations exacerbate illegal logging by creating access roads into remote forest areas. Mining concessions promote land grabbing and human rights violations, mainly those of indigionous peoples. Concerns over toxic waste and biodiversity loss are also not being properly managed. 

![Screenshot 2025-04-02 at 11 44 36](https://github.com/user-attachments/assets/1b9f883d-cbc6-4644-8851-ac8bc228810b)

Figure 5: historic Forest loss of South Prey Lang. The primary colour is red, indicating a higher forest loss post creation of the protected area.
![Screenshot 2025-04-02 at 11 45 14](https://github.com/user-attachments/assets/c3a4e019-b9d3-4a5b-a43d-8d693f854368)
Figure 6: Forest loss over Prey Lang from 2000 - 2024

# Why are new mines cropping up in a protected area?
The historical context of Cambodia’s gold mining industry shows a transition from small-scale artisanal mining to large-scale mechanized operations. While this shift has led to economic benefits, it has also facilitated corruption, human rights violations, and environmental degradation. The 2007 Cambodian government aligned its future income the coorportisation of mining practices, to help alleviate its reliance on foregn aid and loans. This new revenue stream lined the pockets of the party-elite instead of contributing to Cambodian peoples health, infrastructure and economy. Evidenced in 2023 when the Australian National Court fined the previous owner of a large mining concession in Mondulkiri Province, Cambodia $10 million for bribing Cambodian officials. This is almost certainly not an isolated issue. In recent times, global geopolitical instability has fueled a new gold rush, with prices soaring by 28% in 2024, further intensifying mining activity.


![Screenshot 2025-04-02 at 13 12 51](https://github.com/user-attachments/assets/d8ae8dde-62fb-4829-b96e-b554c11fbf87)
Figure 7: older concessions show the potential damage to biodiversity 10 years can have. New concessions that are deeper in the forest may follow this trend.


# Citations

Villa, L. et al. (2024). Monitoring Gold Mining Activity Using SAR. In: Cardille, J.A., Crowley, M.A., Saah, D., Clinton, N.E. (eds) Cloud-Based Remote Sensing with Google Earth Engine. Springer, Cham. 

Pauly, M., Crosse, W. & Tosteson, J. High deforestation trajectories in Cambodia slowly transformed through economic land concession restrictions and strategic execution of REDD+ protected areas. Sci Rep 12, 17102 (2022)



