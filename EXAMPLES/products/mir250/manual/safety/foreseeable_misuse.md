# Foreseeable misuse {% tag="forseeable_miuse" %}

{% partial file="partials/safety/list_forseeable_miuse.md" /%}

{% partial file="partials/references/info_environmental_factors_evaluate_environment_commissioning.md" /%}

{% if and($is_deckload, not($top_module)) %}

## Unsupported top modules

It is also foreseeable misuse to connect unsupported top modules to the robot. This includes, but is not limited to:

* Any MiR top modules that are not specifically designed for {% $model %}
* Top modules that do not meet the electrical requirements in {% tagref tag="electrical_interfaces" /%}
* Top modules that are not within the payload distribution described in {% tagref tag="payload_distribution" /%}

{% /if %}

{% if $is_forklift %}

## Unsupported payloads and handling

It is also foreseeable misuse to make the robot transporting unsupported loads or handling loads in unsupported ways. This includes, but is not limited to:

* Making the robot tow loads
* Using the robot to stack pallets or to pick up pallets from stacks
* Transporting pallets not fulfilling the technical specifications—see {% tagref tag="payload_distribution" /%}

{% /if %}
