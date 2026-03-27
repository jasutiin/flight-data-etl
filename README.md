learning what an etl pipeline is and using power bi to visualize the data

the visualizations i want to make:
- busiest airports
- top 10 most frequently aircraft types that arrive at/depart from an airport
- average time an aircraft spends in the air vs. grounded

the 3 visualizations above i got from claude, but lowkey i need to practice reading data and seeing what i can derive from it so here's the stuff i came up with:
- nothing so far

using this btw: https://openskynetwork.github.io/opensky-api/rest.html

how it works:
- every hour, it runs the github action
- `extract.py` calls any opensky api endpoint, calls them, and creates a new .csv for the response and adds the .csv to `data/`
- `transform.py` takes the data and transforms it, adds it to `data-transformed/`
- `load.py` takes each .csv and adds it to database
- power bi does its visualization magic