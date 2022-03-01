# mobility_granollers

## Calculs

  1. Estadística bàsica:  Distància total, Temps total, velocitat mitja (+ std), radi de gir, turtuosita
  2. Dos eines de visualització de mapas: Folium (visualitzacions interactives) i OSMXN, OpenStreetMaps Network (en format xarxes i capes). 
  3. Visualitzacions en Mapes de les trajectòries (FOLIUM i OSMNX).
  4. Mapes de calor de les posicions (colors més intensos volen dir més localitzacions en aquella regió) (FOLIUM i OSMNX).
  5. Mapes de calor de les posicions depenent de la velocitat (colors més intensos indiquen una velocitat més elevada en aquella regió) (FOLIUM i OSMNX).
  6. Mapa de calor TimeLapse. Es pot veure com evoluciona el mapa de calor amb el temps. Útil quan tenim diverses trajectòries que es realitzen simultàneament (FOLIUM).
  7. Amb l'OSMNX, es pot recrear un video animació en .mp4 de les trajectòries realitzades (OSMNX).
  8. Criteri per considerar parades temporals: Degut error precisió GPS, és difícil interpretar quan un usuari està parat. Proposem un mètode per escollir una "velocitat llindar"      per sota de la qual considerem que en un punt concret l'usuari es troba quiet. Es pot recalcular tota l'estadística considerant només els punts en moviment.
      

      
      

  
