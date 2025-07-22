There is an adjustment in mining difficulty every 2016 [[Block]]s to ensure we get one [[Block]] every 10 minutes.
$2016 * 10 = 20160$ which is difficulty adjustment every 2 weeks. 

### Difficulty adjustment
Let's call 2016 $ExpectedDifficulty$. Then $DifficultyAdjustment = ExpectedDifficulty / {ActualBlocksFor2Weeks}$.
For example, if $ActualBlocksFor2Weeks$ is 1500 (1500 blocks are mined for 2 weeks in this case), then $DifficultyAdjustment = 2016 / 1500 = 1.344$.
**Note**: $DifficultyAdjustment \leq 4$   

### Actual difficulty
$NewDifficulty = OldDifficulty * DifficultyAdjustment$ 