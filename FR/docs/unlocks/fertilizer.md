# Engrais
À un certain moment, attendre que les plantes poussent n'est plus assez efficace. 
Comme pour l'eau, tu recevras automatiquement 1 engrais toutes les 10 secondes, plus un supplémentaire pour chaque amélioration.

L'engrais peut faire pousser les plantes instantanément. `use_item(Items.Fertilizer)` réduit le temps de croissance restant de la plante sous le drone de 2 secondes.

Cela a quelques effets secondaires.
Les plantes cultivées avec de l'engrais seront infectées.

Lorsqu'une plante est infectée, la moitié de sa récolte est transformée en `Items.Weird_Substance` lorsqu'elle est récoltée.
La Substance Étrange peut également être utilisée sur les plantes, ce qui a pour effet de changer le statut infecté de la plante et de toutes les plantes adjacentes.

Donc, si tu appelles `use_item(Items.Weird_Substance)` sur une plante infectée, cela la guérira, mais si tu l'utilises sur une plante saine, cela l'infectera.

Si tu l'utilises sur une plante infectée qui a des voisines saines, cela guérira la plante mais infectera les voisines et vice versa.