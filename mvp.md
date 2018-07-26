### MVP Proposal

## Domain

I'm looking at classifying mushrooms as poisonous or edible based on an extensive list of features provided by Kaggle. I'm not familiar with classifying mushrooms, although I do know about a few of the primary indicators to indicate super poisonous mushrooms locally (odor and gill markings). I'm also aware that most mushrooms need to be cooked in order to be palatable, which I'm assuming this dataset holds as an assumption.

## Data

This dataset includes 23 species of gilled mushrooms in two genera (Agaricus and Lepiota) of common mushrooms. This represents a small subset of mushrooms, so it doesn't generalize to all mushroom species. The overview of the dataset also mentions that there's no simple way of classifying poisonous mushrooms (compared to poison oak), so any analysis would be restricted to this data.

The dependent variable is binary: poisonous/safe and includes 22 independent variables, all classes. I'd like to utilize all of these variables except for Veil type (no relation to dependent variable), and it seems like this is a solved problem (via logistic regression), at least in terms of this dataset. The specific independent variables are as follows:


| Variable                    | Classes        |
| --------------------------- |:-------------:|
| Cap shape                   | Bell, conical, convex, flat, knobbed, sunken |
| Cap surface                 | Fibrous, grooves, scaly, smooth      |  
| Cap color                   | Brown, buff, cinnamon, gray, green, pink, purple, red, white, yellow  |
| Bruises                     | Yes, no |
| Odor                        | Almond, anise, creosote, fishy, foul, musty, none, pungent, spicy      |  
| Gill attachment             | Attached, descending, free, notched      |
| Gill spacing                | Close, crowded, distant |
| Gill size                   | Broad, narrow      |  
| Gill color                  | Black, brown, buff, chocolate, gray, green, orange, pink, purple, red, white, yellow     |
| Stalk shape                 | Enlarging, tapering |
| Stalk root                  | Bulbous, club, cup, equal, rhizomorphs, rooted, missing      |  
| Stalk surface above ring    | Fibrous, scaly, silky, smooth     |
| Stalk surface below ring    | Fibrous, scaly, silky, smooth |
| Stalk color above ring      | Brown, buff, cinnamon, gray, orange, pink, red, white, yellow      |  
| Stalk color below ring      | Brown, buff, cinnamon, gray, orange, pink, red, white, yellow      |
| Veil type                   | Partial, universal      |
| Veil color                  | Brown, orange, white, yellow |
| Ring number                 | None, one, two      |  
| Ring type                   | Cobwebby, evanescent, flaring, large, none, pendant, sheathing, zone     |
| Spore print color           | Black, brown, buff, chocolate, green, orange, purple, white, yellow |
| Population                  | Abundant, clustered, numerous, scattered, several, solitary      |  
| Habitat                     | Grasses, leaves, meadows, paths, urban, waste, woods     |

## Known unknowns

* Find additional data - Considering my initial model (logistic regression) yielded a perfect score, I'd like to try to find another set of labeled data to validate or at least contextualize my model. It's likely this won't be easy, I may need to do it manually via the book the original dataset was aggregated from.

* Plot a 3D classification graph of the dataset to see if the feature with 0-correlation is easy to spot.

* Test other models, specifically SVM, to see if it's a relevant/reasonable model for this data.
