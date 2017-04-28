# jon~
Pure Data reverb abstraction based on "Simplified plate-class reverberation topology in the style of Griesinger" from the article "Effect Design, Part 1: Reverberator and Other Filters" by Jon Dattorro.

## Implementation details

In order to make the implementation sample rate independent the fixed sample delay values in the original figure was converted by dividing the values with the suggested sample rate. Below, complete conversion table:

                  smp   /29.761

input diffusion allpass filters:

13_14             142   4,77134
19_20             107   3,59530
15_16             379   12,7348
21_22             277   9,30748


tank allpass filters:

23_24             672   22,57988
24_30             4453  149,62534
31_33             1800  60,48183
33_39             3720  124,99579

46_48             908   30,50972
48_54             4217  141,69550
55_59             2656  89,24431
59_63             3163  106,28003

excursion         16    0,53761

taps:

yl
48_54           + 266   8,93787
48_54           + 2974  99,92943
55_59           - 1913  64,27875
59_63           + 1996  67,06763
24_30           - 1990  66,86603
31_33           - 187   6,28339
33_39           - 1066  35,81868

yr
24_30           + 353   11,86116
24_30           + 3627  121,87090
31_33           - 1228  41,26205
33_39           + 2673  89,81553
48_54           - 2111  70,93175
55_59           - 335   11,25634
59_63           - 121   4,06572


