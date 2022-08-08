---
widget: slider
weight: 20
active: true
headless: true

design:
  # Slide height is automatic unless you force a specific height (e.g. '400px')
  slide_height: ''
  is_fullscreen: true
  # Automatically transition through slides?
  loop: false
  # Duration of transition between slides (in ms)
  interval: 2000

content:
  slides:
    - title: 'Axe 1 : Imagerie médicale'
      content: 'xxx'
      align: center
      background:
        position: right
        color: '#666'
        brightness: 0.7
        media: imagerie_medicale.png
    - title: 'Axe 2 : Données hétérogènes'
      content: 'yyy'
      align: left
      background:
        position: center
        color: '#555'
        brightness: 0.7
        media: donnees_heterogenes.png
    - title: 'Axe 3 : Apprentissage fédéré'
      content: 'zzz'
      align: right
      background:
        position: center
        color: '#333'
        brightness: 0.5
        media: apprentissage_federe.png
---
