# Mongodb Drills


## Find the listing detail information for the Evernote app?

{% mongoquery %}

{"n":"com.evernote"}

{% endmongoquery %}

{{ data | json }}

There are {{ data.length }} apps.
The star rating of the first Evernote app is: {{ data[0].rate }}

## How many apps developed by GO Launcher EX?
{% mongoquery %}

{"crt":"GO Launcher EX"},{"n":1}

{% endmongoquery %}

{{ data | json }}

There are {{ data.length }} apps.

## How many apps have been downloaded more than 10,000,000?
{% mongoquery %}

{% endmongoquery %}

{{ data | json }}

(answer)

## How many apps have the word "share" in their description?
{% mongoquery %}

{% endmongoquery %}

{{ data | json }}

(answer)

## Find apps that are categorized in any of the following categories: Productivity, Business, or Finance?
{% mongoquery %}

{% endmongoquery %}

{{ data | json }}

(answer)
