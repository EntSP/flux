# Product presentation {% tag="product_presentation" %}

{% if and($is_deckload, not($top_module)) %}
{% $model %} is a component which is designed to be used as a generic base when designing an autonomous mobile robot (AMR) for a specific application. The structure and electrical interfaces allow a wide variety of top modules to be designed and integrated so that it forms a complete AMR.
{% /if %}

{% if $is_forklift %}
{% $model %} is an autonomous mobile robot that can transport loaded pallets indoors within production facilities, warehouses, and other industrial locations where access to the public is restricted. The robot can pick up and place supported pallets—see {% tagref tag="payload_distribution" /%} from the floor or pallet stations that meet the specifications in {% tagref tag="pallet_transfer_stations" /%}
{% /if %}

{% partial file="partials/common/text_safety_function_features_for_amr_material_handling.md" /%}

{% partial file="partials/common/text_pcm_intended_for_incorporation.md" /%}