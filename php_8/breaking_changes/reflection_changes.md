# Reflection changes

Certaines méthodes ont eté dépréciées
 - ReflectionFunction::isDisabled()
 - ReflectionParameter::getClass()
 - ReflectionParameter::isCallable()

Il faut à présent utiliser ReflexionType pour avoir des 
informations sur le type d'un paramètre
