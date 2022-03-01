# mobility_granollers

## Calculs

  1. Estadística bàsica:  Distància total, Temps total, velocitat mitja (+ std), radi de gir, turtuosita
 
  2. Dos eines de visualització de mapas: Folium i OpenStreetMaps Network.
  
      2.1 - Folium. És una eina de visualització de trajectòries i mapes de calor en un mapa interactiu en format .html  Es útil perquè proporciona una visualització xula, neta             i detallada.
     
      2.2 - OSMNX (Open Street Maps Networks). És un paquet de Python on podem importar les xarxes dels carrers d'una determinada zona. No proporciona una visualització dels                 carrers amb tant detall ni tant neta com els mapes de Folium. Però és més util per treballar amb les coordenades dins dels mapes.
     
  3. Amb el Folium, realitzem les següents visualitzacions en mapes:
      3.1 - Mapa de visualització de les trajectòries (en forma de línia contínua)
      3.2 - Mapa de calor de visualització de les trajectòries. És colors més intensos volen dir que allà hi ha més localitzacions GPS. 
      3.3 - Mapa de calor depenent de les velocitats. Mapa de calor de les trajectòries, pero utilitzant la velocitat per la intensitat de la calor, aquelles zones on la                     velocitat és més elevada, són més intenses.
      3.4 - Mapa de calor TimeLapse. És poden recrear els mapes de calors anteriors en format vídeo (time-lapse). És a dir, com evoluciona el mapa de calor amb el temps. És útil             quan tenim diverses trajectòries que s'estan realitzant simultàneament (el cas del dia de la festa). D'aquesta manera es pot veure en els intervals de temps                     desitjats (per exemple cada minut) com evoluciona el mapa de calor de totes les localitzacions GPS.
     
  4. Amb l'OpenStreetMaps, realitzem les següents visualitzacions en mapes:
      4.1 - Visualització de les trajèctories en punts o en forma de línia (en Folium no hem aconseguit veure-ho per punts separats).
      4.2 - Mapa de calor (com 3.2 i 3.3) però en aquest cas no és de manera interactiva (amb zoom), sinó estàtica i per punts.
      4.3 - Video animació en .mp4 de les trajectories realitzades.

  5. Criteri per considerar parades temporals. 
      Degut, obviament, a un error sempre present en la medició de la posició a través dels satèl·lits GPS, pot resultar difícil saber quan analitzem una trajectòria en quins          moments l'usuari ha realitzat una parada. Per molt que estigui en la mateixa posició, hi ha un error en la mesura, que pot ser d'uns metres, i el dispositiu seguirà              enregistrant localitzacions amb unes distàncies i velocitats entre elles diferents de zero.
      
      Utilitzem el següent criteri per determinar si un usuari està parat o en moviment: Suposem que hi ha una "velocitat llindar" per sota de la qual considerem que l'usuari en       aquell punt està quiet (o en moviment si la velocitat és major que la llindar). Aleshores, calculem, per un ventall ampli de velocitats llindars, quantes localitzacions es       troben en "stop". Per velocitats llindars molt petites (properes a 0) és obvi pensar que el nombre de "stops" és pràcticament inexistent, ja que la major part de                 localitzacions tenen una velocitat més gran que 0. En cas contrari, si escollim una velocitat llindar molt alta, totes les velocitats es trobaran per sota i per tant el         100% de les dades es consideraran "stops". Per tant, una manera útil d'escollir la velocitat llindar adecuada, és representant el nombre de stops en funció d'un ventall         ampli de velocitats llindars, i veure on hi ha un canvi de comportament en la funció. En altres paraules, on es troba el punt d'inflexió on el nombre de "stops" pasa de         crèixer a saturar-se? Aquest punt marca el valor "ideal" de la velocitat llindar.
      
      

  
