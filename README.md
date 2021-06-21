# verifyvartype
Exercice : vérifier  si une  variable est d'un certain type 
Pour vérifier si une variable est d'un certain type, on peut utiliser la fonction type ou la fonction isinstance.

On vérifie une première fois si la variable "prenom" est de type "str", c'est le cas, la phrase "La variable est une chaîne de caractères" s'affiche donc bien à l'écran.

On redéfinie ensuite la variable "prenom" pour lui assigner le nombre 0.

On vérifie ensuite une deuxième fois avec la fonction isinstance, que la variable "prenom" est bien une instance de la classe "str". Cette fois-ci, la variable "prenom" étant égale à un nombre entier (int), la phrase ne s'affiche pas.

Dans un exemple simple comme celui-ci, le résultat est similaire. Il est cependant préférable d'utiliser la fonction isinstance, car elle fonctionnera également si vous vérifier le type d'une variable qui hérite d'une classe qui est du type que vous cherchez.

    >>> default_dict = {}
     
    >>> type(default_dict)  # Notre dictionnaire est bien de type 'dict'
    <type 'dict'>
     
    >>> class CustomDict(dict):  # On créé une classe custom, qui hérite de la classe 'dict'
    ...     pass
     
    >>> custom_dict = CustomDict()
     
    >>> type(custom_dict)
    <class '__main__.CustomDict'>
     
    # Avec la fonction type(), notre dictionnaire custom n'est pas reconnu comme étant de type 'dict'
    >>> type(custom_dict) == dict
    False                     
     
    # La fonction isinstance en revanche comprend que notre dictionnaire custom hérite de la classe 'dict'
    >>> isinstance(custom_dict, dict)
    True                      
