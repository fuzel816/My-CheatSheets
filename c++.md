# Einfügen eines Vektorelements via Referenz

``` c++
vector<Node> nodesObj;

for (auto &elem : listOfNodeIps) {
  nodesObj.emplace_back(elem, argv); //Pass the extracted ips to call netopper-cli
}
```

# Einsatz von Shared Pointern

+ Shared pointer beinhalten die Referenz auf eine Klasse.
+ Die Klasse existiert bis alle Referenzhalter nicht mehr existieren

+ Deklarieren eines shared pointer vektors in einer Klasse
``` c++
vector < shared_ptr<Port> >ptrToPortVec;
```
+ Erstellen eines shared pointers in einer Methode
``` c++
auto sp = make_shared<Port>(elem.node().child_value());
```
+ Befüllen des Vektors über eine erstellte Instanz
``` c++
nodeObjVec[i].ptrToPortVec.emplace_back(sp);
```
