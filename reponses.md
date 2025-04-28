# Que constates-tu ?

3. Quelle est l'utilité de ce répertoire ?

Il sert à pouvoir définir des workflows GitHub Actions. Un workflow est un ensemble d'automatisations (par exemple, tester ton code, le déployer, etc.).


8. Accède à l'onglet "Actions" de ton repository sur GitHub. Que constates-tu ?

Il y a un workflow qui a été créer dans mon repository qui porte le nom de "Hello World".

10. Commit et pousse ce nouveau workflow. Vérifie l'exécution dans l'onglet Actions. Que constates-tu ?

Il y a un nouveau workflow qui a été créer, qui s'appelle Run Tests

11. Modifie le fichier model.py pour introduire un bug (change le retour de "positive" à "positif" par exemple). Que se passe-t-il lors du prochain push ?

J'ai une erreur :
Run pytest
============================= test session starts ==============================
platform linux -- Python 3.10.17, pytest-7.3.1, pluggy-1.5.0
rootdir: /home/runner/work/github-actions-tp1/github-actions-tp1
collected 3 items

test_model.py F..                                                        [100%]

=================================== FAILURES ===================================
____________________________ test_predict_positive _____________________________

    def test_predict_positive():
>       assert predict_sentiment("I am happy today") == "positive"
E       AssertionError: assert 'positif' == 'positive'
E         - positive
E         ?       ^^
E         + positif
E         ?       ^

test_model.py:6: AssertionError
=========================== short test summary info ============================
FAILED test_model.py::test_predict_positive - AssertionError: assert 'positif' == 'positive'
  - positive
  ?       ^^
  + positif
  ?       ^
========================= 1 failed, 2 passed in 0.03s ==========================



14.  Que constates-tu après le push ?

![capture workflow_test](/assets/1_workflow_test.PNG)

