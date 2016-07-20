Why towel?
-----
> A towel is about the most massively useful thing an interstellar hitchhiker can have. Partly it has great practical value. You can wrap it around you for warmth as you bound across the cold moons of Jaglan Beta; you can lie on it on the brilliant marble-sanded beaches of Santraginus V, inhaling the heady sea vapors; you can sleep under it beneath the stars which shine so redly on the desert world of Kakrafoon; use it to sail a miniraft down the slow heavy River Moth; wet it for use in hand-to-hand-combat; wrap it round your head to ward off noxious fumes or avoid the gaze of the Ravenous Bugblatter Beast of Traal (such a mind-boggingly stupid animal, it assumes that if you can't see it, it can't see you); you can wave your towel in emergencies as a distress signal, and of course dry yourself off with it if it still seems to be clean enough.
                                                                                                
                                                                   -- The Hitchhiker's Guide to the Galaxy

Setting up Towel
-----


1. Installing Elasticsearch:
  + Download and extract Elasticsearch 2.3.4 from [here](https://www.elastic.co/downloads/elasticsearch).
  + You'll also need to install [JAVA](http://java.com/en/download/manual.jsp)
    - If you haven't already, configure JAVA_HOME. (see [instructions](https://confluence.atlassian.com/doc/setting-the-java_home-variable-in-windows-8895.html))
  + To run ES, we run `elasticsearch.bat` located in the bin folder (in elasticsearch the directory) from a command window. This will start ElasticSearch running in the foreground in the console, meaning we'll see errors in the console and can shut it down using `CTRL+C`. *Note: We don't have to start this manually. Our code will automatically spawn an ES process if its not running already.*
  + Append `X:\<elasticsearch-directory>\bin\` folder to windows PATH (update PATH variable in *Control Panel > System > Advanced System Settings > Environment Variables*)
  + To get started with Elastisearch, a lots of cool resources are available in elastic.co and a good introduction [here](http://joelabrahamsson.com/elasticsearch-101/).
  
2. Setting up Python:
  + We use anaconda by continuum.io (see [Why?](https://www.continuum.io/why-anaconda))
    - We won't need the entire distribution. [Download](http://conda.pydata.org/miniconda.html) & install a minimal version of anaconda.
  + Make sure you select add to PATH during install.
  + Next, navigate to towel, and run `setup.bat`. This will install all the dependencies needed to run the sandbox.

3. Running script:
  + Navigate to *src > site* and run `index.py`
  
      ```
      Usage: python -B index.py [OPTIONS]
      Options:
        --debug   BOOLEAN    Flags: True/False. Render site in debug mode. Default True.
        --force   BOOLEAN    Flags: True/False. Create force injest documents to ES. Default False.
                                  Atchung! Set TRUE only if injest.py has been change, otherwise 
                                  several (unnecessary) injestions may occur. 
        --port    INTEGER    Port to deploy the site on. Default 8000.
        --verbose BOOLEAN    Flags: True/False. Display all outputs to stdout. Default True.
      ```
  
  
    
