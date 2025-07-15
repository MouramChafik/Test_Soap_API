# Test API SOAP

Ce projet contient des tests automatisés pour une API SOAP calculator 
"http://www.dneonline.com/calculator.asmx?WSDL"




## Lancer les tests

Pour exécuter les tests, utilisez la commande suivante :

```bash
testrunner.sh -s "CalculatorSoap TestSuite" testsoap-soapui-project.xml 
```
## Générer les rapports

Pour générer les rapports de test SOAP, utilisez la commande suivante qui inclut le flag -j pour le format JUnit et -f pour spécifier le dossier de sortie :

```bash
testrunner.sh -s "CalculatorSoap TestSuite" -j -f Reports testsoap-soapui-project.xml 
```

Les rapports seront générés dans le dossier `Reports/`.

## Intégration Continue avec GitHub Actions

Les tests sont automatiquement exécutés via GitHub Actions à chaque push sur le repository. Le workflow :

- Lance les tests SOAP
- Génère les rapports
- Archive les résultats des tests

Vous pouvez consulter les résultats des tests dans l'onglet "Actions" du repository GitHub.
