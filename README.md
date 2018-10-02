
# Uvod
Za razvojno okolje sem uporabil Visual Studio 2015 s programskim jezikom Python različice 3.5.

Prvi korak je bil prenos modela YOLO in sprememba razreda predikcije objektov v avtomobile("car").

Sprememba funkcionalnosti glavnega programa iz zajema sekvence slik iz kamere na branje videa iz datoteke. 

Izris okvirjev okoli zaznanega objekta ter pripadajočo unikatno identifikacisjko številko(ID).

Grafični prikaz verjetnosti detekcije objekta.

Zapis pozicije zaznanega objekta v slikovnih točkah, pripadajoči ID in v katerem slikovnem okviru se je detekcija pojavila.
Datoteka: sledenje.txt

Potrebne izboljšave:
Optimizacija parametrov sledenja objektom in detekcije objektov.
Preverjanje vrednosti pozicije v slikovnih točkah(Določene točke imajo negativno vrednost kar ni mogoče. Predvidevam da gre za motnjo pri inicializaciji filtra sledenja  objetkom.)

Podrobnejše preverjanje rezultatov zanesljivosti detekcije objektov. Vrednost je ves čas 1, kar pa je praktično nemogoče in ne predstavlja kredibilnega podatka. Yolo.scores poda Tensor spremenljivko verjetnosti objekta, katere pa nisem uspel interpretirati. Težave s pretvorbo tipa spremeljivk. Predvidevam nekompatibilnost različic knjižnic.

Modificirane datoteke: demo.py, yolo.py
Rezultati: tekstovna datoteka sledenje.txt
           video posnetek z dodanimi grafičnimi informacijami output.avi

# Zagon

Naložen je celoten projekt ki ga je moč zagnati v Visual Studio 2015 ali novejše. Zaradi prevelike velikosti datoteke, na repozitoriju manjka datoteka modelov razpoznavanja: https://drive.google.com/file/d/1uvXFacPnrSMw6ldWTyLLjGLETlEsUvcE/view?usp=sharing


  ```

# Knjižnice:
  Keras 2.2.2
  NumPy 1.15.2
  OpenCV-Python 3.4.3.18
  SciPy 1.1.0
  Tensorflow 1.11.0
  Pillow 5.3.0


 

