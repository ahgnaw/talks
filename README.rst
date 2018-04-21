A collection of resources from talks I will or may, present.

Each talk will have different minimum requirements, so each folder will have virtual environment setups.

Princeton Quant Trading
-----------------------

The jypyter notebooks in folder ``princeton_quant_trading``  use python 3.6 and pipenv.

To setup resources:

::

    cd princeton_quant_trading
    pipenv install
    pipenv shell


To run the notebook used to create the diagrams on the slides:

::

    jupyter notebook


The jupyter notebook app will launch in your browser. Click on ``graphs.ipynb``.
Here you can view the steps used to create the graphs in the presentation. You can also go to ``Kernel`` -> ``Restart & Clear Output`` to run each cell at a time.

The sqlite3 file ``regular_season.sqlite`` contains data from the regular season 2017-2018 has the tables with the following schemas:

:: 

    sqlite> .schema player_game_log
    CREATE TABLE player_game_log
                (
                    name TEXT,
                    position TEXT,
                    opponent TEXT,
                    game_date TEXT,
                    salary INTEGER,
                    score REAL,
                    minutes INTEGER,
                    points INTEGER,
                    made_3pt INTEGER,
                    rebound INTEGER,
                    assist INTEGER,
                    steal INTEGER,
                    block INTEGER,
                    turnover INTEGER,
                    double_double INTEGER,
                    triple_double INTEGER
                );
    sqlite> .schema players
    CREATE TABLE players
                (
                    name TEXT,
                    team TEXT,
                    birth_date TEXT,
                    height INTEGER,
                    weight INTEGER
                );
    sqlite> .schema team_game_log
    CREATE TABLE team_game_log
                (
                    name TEXT,
                    abbr TEXT,
                    game_date TEXT,
                    opponent TEXT,
                    home INTEGER,
                    win INTEGER,
                    points INTEGER
                );


