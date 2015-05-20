
PROJET IDM M2PGI : SQLSCRIBE
===========================

XML -> MODELIO
---------------

Le script est nomm� **project_IDM_xml2modelio**. Le fichier source est **macros/project_IDM_xml2modelio.py**. 

Les pr�-requis sont :

	* Un projet doit �tre ouvert et s�lectionn�.
	
	* Un package nomm� "PackageScribeSQL" doit exist�.
	
	* Les st�r�otypes "PK" (Attribute), "FK" (Attribute), "FKC" (Dependency) et "Table" (Class) doivent exist�s.
	
	* Un fichier **bdd.xml** doit se trouver dans le r�pertoire **lib/res/xml/**
	
Attention, si le package "PackageScribeSQL" n'est pas vide au lancement du script, le contenu sera supprim� !

Le r�sultat se trouve dans le package "PackageScribeSQL".

Remarque : pour afficher les liens des cl�s �trang�res (foreign key) sur le diagramme, il faire **Unmask -> Non structuring link**.

MODELIO -> SQL
---------------

Le script est nomm� **project_IDM_modelio2sql**. Le fichier source est **macros/project_IDM_modelio2sql.py**. 

Les pr�-requis sont :

	* Un projet doit �tre ouvert et s�lectionn�.
	
	* Un package nomm� "PackageScribeSQL" doit exist� et �tre s�lectionn�.
	
	* Le format du contenu du package "PackageScribeSQL" doit correspondre au format g�n�r� par le script **project_IDM_xml2modelio** : une table = une classe, stereotype "PK" sur les cl�s primaires, st�r�otype "FK" sur les cl�s �trang�res, utilisation des "dependency" etc ...
	
Le r�sultat est directement afficher dans la console.