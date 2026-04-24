# Light indicators and speaker{% tag="light_indicator_and_speaker" %}

{% partial file="partials/sounds_lights/text_sounds_and_light_adjusted_during_commissioing.md" /%}

The robot uses its speaker and of light indicators to communicate its status and intentions:

* **Status lights**: LED light bands on all four sides of the robot use colors and patterns to signal the robot's current status.

* **Signal lights**: Lights at the front and back of the robot indicate turning and backward movement. Front lights are white, rear lights are red, and blinking indicates turns.

* **Speaker**: Plays sounds to alert personnel. Can be triggered by zones, mission actions, or when Protective fields are muted.

{% image src=$image_light_indicators_labeled alt="Identification of the light types."  /%}

| Pos. | Description | Pos. | Description |
| --- | --- | --- | --- |
| 1 | Signal lights | 2 | Status lights |

## Status lights

The LED light bands around the robot indicate its operational state:

{% lightindicators /%}

When battery is critically low (0-1%), the ends of the status lights flash red.

## Signal lights

{% partial file="partials/sounds_lights/list_signal_light_behavior.md" /%}

{% notice type="warning" %}
If the robot starts up unexpectedly, there is a risk of injury to nearby personnel or damage to equipment.

* Train personnel in the meaning of the signal and status lights.
* Inform personnel that robot flashes its signal lights and emits warning sounds before is starts moving after being at standstill for longer than 10 seconds.
* Adjust the volume of the warning sounds if they cannot be heard.
* Do not disable the Motion warning feature in the robot settings. This will also void certification for the following standards: ISO 3691-4, UL3100, and RIA 15.08

{% /notice %}

## Sounds

Configure standard sounds you can use in missions and zones under **Setup > Sounds**.

{% partial file="partials/sounds_lights/list_when_warning_sounds_play.md" /%}

The safety sound can be adjusted in **System > Settings > Features**.

{% partial file="partials/sounds_lights/warning_adjust_sound_volume.md" /%}