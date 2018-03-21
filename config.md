## config.ini

The config file contains the default options for running bulkVis. There are
three sections: `data`, `plot_opts`, and `labels`.

`[data]` describes the directories used by bulkVis
|Option|Type|Description|
|-:|:-:|:-|
|`data`|string|Path to the bulk-fast5 file directory|
|`out`|string|Path to where read files will be written, this path must exist|

`[plot_opts]` describes default options for the squiggle plot

|Option|Type|Description|
|-:|:-:|:-|
|`wdg_width`|int|The width of the left-hand panel in bulkVis|
|`plot_width`|int|The width of the squiggle plot in pixels|
|`plot_height`|int|The height of the squiggle plot in pixels|
|`y_min`|int|The minimum value of the y-axis, when this axis is fixed|
|`y_max`|int|The maximum value of the y-axis, when this axis is fixed|
|`label_height`|int|The height, on the y-axis, where labels will be rendered|
|`upper_cut_off`|int|The maximum value that will be plot|
|`lower_cut_off`|int|The minimum value that will be plot|
|`output_backend`|string|This determines how the plot is rendered in the browser; must be one of `canvas`, `svg`, `webgl`|

`[labels]` describes the labels that should be shown by default and which 'jump-to'
options are available these are derived from bulk-fast5 files, specifically the
`IntermediateData` and `StateData` groups. If a classification is not found in a file
it will not be added as an option in the gui...

```INI
[data]
dir = /Users/Alex/projects/bokehApp/bulkvis/data/
out = /Users/Alex/projects/bokehApp/bulkvis/data/make/
[plot_opts]
wdg_width = 300
plot_width = 1600
plot_height = 1000
y_min = 0
y_max = 2200
label_height = 800
upper_cut_off = 2200
lower_cut_off = -1000
; recommended that this is kept as 'canvas' opts: ['canvas', 'svg', 'webgl']
output_backend = canvas
[labels]
adapter = True
mux_uncertain = True
strand1 = False
user1 = True
event = False
user2 = False
multiple = False
unclassed = False
pore = True
strand = True
transition = True
unavailable = False
zero = False
saturated = False
unblocking = True
good_single = False
below = False
above = True
inrange = False
unclassified = False
unclassified_following_reset = False
pending_manual_reset = False
pending_mux_change = False
```