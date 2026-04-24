# Safety functions and interfaces {% tag="safety_functions" %}

The robot's safety system is designed to mitigate significant hazards which could lead to injury.

{% if $is_deckload %}
For an overview of all the safety functions and the PFHd, PL, and Architecture as defined by ISO 13849-1:2015 of each function, see {% tagref tag="safety_functions_overview" /%}.
{% /if %}

{% if and($is_deckload, not($top_module)) %}
Using the safety-rated interfaces requires proper design and validation in accordance with ISO 13849-1 and ISO 13849-2 respectively.
{% /if %}

{% partial file="partials/references/text_wiring_diagrams_system_overview.md" /%}