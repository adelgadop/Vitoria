# Vitoria
A Região Metropolitana de Vitória tem diferentes fontes de emissão onde é importante avaliar o comportamento da poluição do ar. Neste repositório temos a aplicação dos modelos WRF-SMOKE-CMAQ como parte da disciplina de Modelagem de Qualidade do ar da UFMG (segundo semestre 2022).

## Objetivos
Avaliar a poluição do ar com a simulação da qualidade do ar com os modelos WRF-SMOKE-CMAQ.

## To do list
- [ ] Rodar WRF-ARW 4.4.1 para Vitória com dois dominios centrado no aeroporto de Vitória e avaliar as simulações meteorológicas com as observações, periodo 2015_08_30:00 até 2015_09_10:00: 
> Domínio 01: 9 km x 9 km, pontos de grade horizontal 110 x 110. Vertical 36 (mínimo 32 para [FNL GFS 0.25, ds.083.3](https://rda.ucar.edu/datasets/ds083.3/)).
> Domínio 02: 3 km x 3 km, pontos de grade horizontal 112 x 112.
- [ ] Gerar arquivos de emissões com o modelo [SMOKE](https://www.cmascenter.org/smoke/)
- [ ] Rodar CMAQ para Vitória e avaliar as simulações das concentrações dos poluentes com as observações disponíveis. Considerar que nem todas as estações amostram poluentes que representam espacialmente a escala espacial do modelo, podemos ter erros de representação conforme com Brasseur et al. (2017).

### Metodología do GitHub
Em `Issues` você pode escrever dúvidas e a gente pode responder. Em `Wiki` podemos escrever detalhes que não são relevantes mais importantes como baixar dados, instalar programas. Se vc deseja salvar seu `access token` e usuário, escrever `git config --global credential.helper store`, com isso somente vai escrever uma vez o usuário e senha, ja não será necessário depois.

  1. Criar branch para mudanças locais e trabalhar nele.  
     - `git checkout <branch name>`
  2. Trabalhamos nosso `branch`:
     - `git add -A`
     - `git commit -m "Descrição e.g. Novo script XX"`
     - `git push`
  3. O quando você faz `push` vai se criar um `pull request`
  4. Logo se não tem problemas com o `main` você pode fazer um `merge pull request` (Desde o Github)
  5. Atualizado o main:
     - Atualizamos o branch:
        - `git checkout <branch name`
        - `git merge origin/main`
     - Fazemos testes nosso branch
        - `git checkout <branch-name>`
        - `git add -A`
        - `git commit -m ""`
        - `git push`
        - Voltamos ao ponto 3 - 4.
