# Building a Perfect Mushroom Classifier

> ## *5/11/2019*

### Abstract
> Derived from the Audubon Society Field Guide this data set includes physical descriptions of hypothetical samples corresponding to 23 species of gilled mushrooms in the Agaricus and Lepiota Family. Each species is identified as definitely edible, definitely poisonous, or of unknown edibility and not recommended. This latter class was combined with the poisonous one. The guide clearly states that there is no simple rule for determining the edibility of a mushroom; no rule like “leaflets three, let it be” as for Poisonous Oak and Ivy. The goal of this report is to determine the acceptable criteria for mushroom edibility using various machine learning models and if applicable, even a clever mnemonic.
>

### Attribute Information:
> The first version of your mobile app needs to offer a simple and intuitive user experience. Choosing features for your mobile app is a planning process that requires you to define the product vision, objectives, and themes fully. Some standard features can include:

> * class: edible, poisonous.
> * cap_shape: bell, conical, convex, flat, knobbed, sunken.
> * cap_surface: fibrous, grooves, scaly, smooth.
> * cap_color: brown, buff, cinnamon, gray, green, pink, purple, red, white, yellow.
> * bruises: yes, no.
> * odor: almond, anise, creosote, fishy, foul, musty, none, pungent, spicy.
> * gill_attachment: attached, descending, free, notched.
> * gill_spacing: close, crowded, distant.
> * gill_size: broad, narrow.
> * gill_color: black, brown, buff, chocolate, gray, green, orange, pink, purple, red, white, yellow.
> * stalk_shape: enlarging, tapering.
> * stalk_root: bulbous, club, cup, equal, rhizomorphs, rooted, ?.
> * stalk_surface_above_ring: fibrous, scaly, silky, smooth.
> * stalk_surface_below_ring: fibrous, scaly, silky, smooth.
> * stalk_color_above_ring: brown, buff, cinnamon, gray, orange, pink, red, white, yellow.
> * stalk_color_below_ring: brown, buff, cinnamon, gray, orange, pink, red, white, yellow.
> * veil_type: partial, universal.
> * veil_color: brown, orange, white, yellow.
> * ring_number: none, one, two.
> * ring_type: cobwebby, evanescent, flaring, large, none, pendant, sheathing, zone.
> * spore_print_color: black, brown, buff, chocolate, green, orange, purple, white, yellow.
> * population: abundant, clustered, numerous, scattered, several, solitary.
> * habitat: grasses, leaves, meadows, paths, urban, waste, woods.

### Pre-processing Data
> The mycology data set contains 8123 instances and has 0.01% missing data. The class distribution in this data set consists of 23 attributes. The mycology data set initially contained categorical variables denoted as a single letter. These values were updated manually to their corresponding full-word definition. This process required many lines of code which are not explicitly included in the body of this report. The function used to achieve this can be found here and is denoted in a source file above. For flexibility, a second numerical form of this data was created using a function which can be found here. For brevity, these are the only two blocks of code not included in this report. We initially analyze the data integrity and find that of the 0.01% missing data in the set, 100% of the missing values are located within the stalk_root attribute. Of these instances, there are a total of 2480 NA values, making the integrity of this class approximately 69%. Through further examination, we also find that there is a 0.00% variance in the veil_type attribute in the mycology data. To improve the performance of our models, these attributes have been removed.


### Conclusion
> Odor is by far the most important variable in terms of mushroom edibility. The Logistic Regression models performed with high accuracy, before optimizing a threshold value to achieve perfect recall. With some fine tuning, a classification tree managed to predict the edibility of mushroom perfectly. The classification tree approach was preferred due to the ease of implementation and interpretability of the results. If you ever find yourself hungry and wondering the forest just remember the simple mnemonic: “When the odor is almond, anise or none the mushroom is clean, unless the spore print color is green”.

> Please review the .pdf file for the full project!
