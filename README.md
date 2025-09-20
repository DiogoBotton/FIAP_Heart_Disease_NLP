# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Nome do projeto
CorAI | Diagnóstico Automatizado – IA no Estetoscópio Digital

## 👨‍🎓 Integrantes: 
- <a href="https://www.linkedin.com/in/bryanjfagundes/">Bryan Fagundes</a>
- <a href="https://br.linkedin.com/in/brenner-fagundes">Brenner Fagundes</a>
- <a href="https://www.linkedin.com/in/diogo-botton-46ba49197/">Diogo Botton</a> 
- <a href="https://www.linkedin.com/in/hyankacoelho/">Hyanka Coelho</a> 
- <a href="https://www.linkedin.com/in/julianahungaro/">Juliana Hungaro Fidelis</a>

## 👩‍🏫 Professores:
### Tutor(a) 
- <a href="https://www.linkedin.com/in/leonardoorabona?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app">Leonardo Ruiz Orabona</a>
### Coordenador(a)
- <a href="https://www.linkedin.com/in/andregodoichiovato/">André Godoi</a>

## 📜 Descrição

O projeto tem como objetivo treinar dois modelos de classificação, sendo eles, um de classificação multiclasse com o intuito de diagnosticar 4 doenças distintas no contexto de doenças cardíacas, sendo elas:
- Infarto.
- Insuficiência Cardíaca.
- Angina.
- Arritmia.

Assim como, um segundo modelo de classificação binária também será treinado para determinar o nível de risco entre:
- Alto risco.
- Baixo risco.

Ambos os modelos serão treinados com a mesma base de dados de relatos de sintomas de pacientes. A base de dados contem dois rótulos: diagnóstico e nível de risco. Cada rótulo será utilizado para objetivos específicos, a coluna *diagnóstico* será utilizada para classificação multiclasse e a coluna *nível de risco* para o modelo de classificação binária.

## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- **src**: Notebooks com os entregáveis.
- **src/dataset**: Dataset com 100 frases sintéticas de sintomas de pacientes `sintomas_doencas_cardiacas.csv`.
- **src/Atv1_Diagnostico**: Notebook `diagnostico.ipynb` com a criação do modelo de classificação, mapa de conhecimento (csv) e o modelo de classificação gerado `modelo_diagnostico_lr_pipeline.joblib`.
- **src/Atv2_Nivel_Risco**: Notebook `nivel_risco.ipynb` com a criação do modelo de classificação binária (alto risco e baixo risco) e o modelo de classificação gerado `modelo_nivel_risco_lr_pipeline.joblib`.

## 🔧 Como executar o código

Para testar os modelos de diagnóstico e classificação de risco importe um dos modelos a partir de um arquivo com extensão `.py` ou `.ipynb` com a biblioteca *joblib* e realize o teste com alguma frase como parâmetro da função *predict*:

````py
from joblib import load

modelo = load('meu_modelo.joblib')

frase = 'estou sentindo uma dor muito forte no peito'

predicao = modelo.predict(frase)

print(predicao) # Retornará o diagnóstico ou o nível de risco dependendo do modelo importado
````

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>