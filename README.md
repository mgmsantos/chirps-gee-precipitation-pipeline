# Extração de Chuva Diária com GEE e Python

Script em Python para extrair séries temporais de precipitação diária (em mm) para polígonos utilizando a API do Google Earth Engine e o produto CHIRPS.

---

### Aplicação em Python

1. **Inicializa o ambiente:** Conecta e autentica na API do Google Earth Engine utilizando o projeto configurado.
2. **Define as áreas de interesse:** Cria uma coleção de feições (`ee.FeatureCollection`) contendo as coordenadas geográficas e os metadados de cada propriedade (identificador, cultura, município e estado).
3. **Filtra a coleção CHIRPS:** Seleciona a banda de precipitação da coleção diária (`UCSB-CHG/CHIRPS/DAILY`) delimitada pelo período de datas e pela localização dos polígonos.
4. **Calcula a média zonal diária:** Executa uma função iterativa com `reduceRegions()` para calcular a lâmina média de precipitação dentro de cada polígono na escala nativa do sensor (~5,5 km), atribuindo a respectiva data a cada medição.
5. **Estrutura os dados:** Achata os resultados (`flatten()`), recupera os dados processados na nuvem e monta um `DataFrame` do Pandas com valores arredondados, tipos corrigidos e ordenação por fazenda e data.

---

### Requisitos

* `earthengine-api`
* `pandas`

## Conecte-se Comigo

*Siga os links abaixo para saber mais sobre minha trajetória profissional e me contatar:*

<div> 
  <a href="mailto:miguel.gms31@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/miguelgms31/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
  <a href="http://lattes.cnpq.br/2943203054995050" target="_blank"><img src="https://img.shields.io/badge/-Lattes-%230077B5?style=for-the-badge&logo=google-scholar&logoColor=white" target="_blank"></a>
</div>

---
