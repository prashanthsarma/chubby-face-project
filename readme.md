A simple problem statement - Can an AI identify or predict atleast 1 aspect of human life based on placement of any 1 single planet placement. We are trying to follow Vedic astrology.

So we have to just create data for various combinations mentioned in the vedic astrology books where the natal Moon is strong. Feed it into an AI program and voila !!

But alas!, it isn't as easy as it seems.

The datamodel is a simple table containing degrees of each planet expressed as a longiture starting from Aires as 0 degrees. So each planet will have a degree going from 0-360. i.e Ascendant, Sun, Moon, Mercury, Venus, Mars, Jupiter, Saturn and Rahu. Ketu is a dependant parameter on Rahu so we dont consider it.



So, over a single weekend tried to create a dataset for different placements of mooon and I have failed miserably. 
As astro books generally speak only in a combination of 2 or 3 planets, but an AI cannot work well with missing data i.e. for each combination of moon, we need to have combination of other planets as well.



The combinations which were chosen were following:
1. Placement of moon in various houses - 1 to 12 from Ascendant. Ascendant itself can be placed in any of 12 signs
2. Benefic aspects from Jupiter, where Jupiter is placed in any of 12 houses
3. Benefic aspects from Venus, where Venus is placed in any of 12 signs
4. Malefic aspects from Saturn, where Saturn is placed in any of 12 houses
5. Malefic aspects from Mars, where Mars is placed in any of 12 houses
6. Malefic aspects from Rahu, where Rahu is placed in any of 12 houses

But the trouble is that for each of these placements, we also need to calculate the placement of other planets, such that it does affect the above combinations - which is where the trouble begings. This is far more effort and cannot be done over a weekend.

As 2 Jun 2024, the current data merely randomizes the placement of other planets - which is incorrect, but worth a try. A complete failure as  the predictions fail and at most is close to 60% probability of identifyin the placement

This data could run into millions of records. The current moon-positions.ipynb generates close to 2,000,000 records and when fed to a simple randome forest or neural network classifier doesn't end up converging for  various parameters.

I am calling it a "Chubby face Project" as well placed moon helps having a well rounded face and also a strong mind. 
