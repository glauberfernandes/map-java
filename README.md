# Map

## Map<K,V>

* https://docs.oracle.com/javase/10/docs/api/java/util/Map.html

* É uma coleção de pares chave / valor
  * Não admite repetições do objeto chave
  * Os elementos são indexados pelo objeto chave (não possuem posição)
  * Acesso, inserção e remoção de elementos são rápidos  
  
* Uso comum: cookies, local storage, qualquer modelo chave-valor  

* Principais implementações:
  * **HashMap** - mais rápido (operações O(1) em tabela hash) e não ordenado
  * **TreeMap** - mais lento (operações O(log(n)) em árvore rubro-negra) e ordenado pelo compareTo do objeto (ou Comparator)
  * **LinkedHashMap** - velocidade intermediária e elementos na ordem em que são adicionados

### Alguns métodos importantes
* put(key, value), remove(key), containsKey(key), get(key)
  * Baseado em equals e hashCode
  * Se equals e hashCode não existir, é usada comparação de ponteiros  
  
* clear()
* size()
* keySet() - retorna um ```Set<K>```
* values() - retorna um ```Collection<V>```

### Exercício proposto

Na contagem de votos de uma eleição, são gerados vários registros
de votação contendo o nome do candidato e a quantidade de votos
(formato .csv) que ele obteve em uma urna de votação. Você deve
fazer um programa para ler os registros de votação a partir de um
arquivo, e daí gerar um relatório consolidado com os totais de cada
candidato.

**Input file example:**
> Alex Blue,15  
Maria Green,22  
Bob Brown,21  
Alex Blue,30  
Bob Brown,15  
Maria Green,27  
Maria Green,22  
Bob Brown,25  
Alex Blue,31  

**Execution:**
> Enter file full path: c:\temp\in.txt  
Alex Blue: 76  
Maria Green: 71  
Bob Brown: 61  
