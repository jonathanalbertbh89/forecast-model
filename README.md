# Configuração Profissional do README para Azure Machine Learning

## Configuração da Conta Azure e Criação do Recurso

1. **Acessando o Azure para Criar Recurso:**
   - Acesse o [portal do Azure](https://portal.azure.com/) após realizar o cadastro.
   - Na barra de pesquisa, digite "Azure Machine Learning".

2. **Criação do Recurso:**
   - Clique em "CREATE" e, em seguida, em "NEW WORKSPACE".
   - Preencha os campos em "Basics":
      - 🌐 **Subscription:** Mantenha sua assinatura do Azure.
      - 🗃️ **Resource group:** Selecione um existente ou crie um novo.
      - 🏢 **Name:** Escolha um nome para seu espaço de trabalho.
      - 🌍 **Region:** Selecione a região mais adequada para o projeto.
      - Mantenha os valores padrão para Storage account, Key vault, Application insights.
      - O Container será criado automaticamente ao implementar um modelo em um container.
   - Clique em "REVIEW + CREATE" e, se estiver tudo correto, em "CREATE".
   - 🕐 Aguarde o deploy com paciência, faça um lanche.

3. **Pós-Deploy:**
   - Após o deploy bem-sucedido, vá para a HOME e clique no seu WORKSPACE.
   - No cliente, clique em "LAUNCH STUDIO" para o próximo passo.

4. **Configuração do Automated ML:**
   - Clique em "AUTOMATED ML" no menu lateral.
   - 🆕 Vá para "NEW AUTOMATED ML JOB".
      - 📋 **Job name:** Informe um nome para o trabalho (ex: mslearn-bike-automl).
      - 🧪 **New experiment name:** Nome do novo experimento (ex: mslearn-bike-rental).
      - 📝 **Description:** Descrição recomendada (Aprendizado de máquina automatizado para previsão de aluguel de bicicletas).
      - Tags: Não é necessário.

5. **Configurações de Tarefa e Dados:**
   - Em "Task type & data":
      - 📊 **Select task type:** Informe "regressão (Regression)".
      - Clique em "CREATE" e selecione um conjunto de dados com as informações fornecidas.
      - 🔄 Clique em "NEXT".
      - Selecione a fonte "From Web files".
      - Informe a URL [https://aka.ms/bike-rentals](https://aka.ms/bike-rentals) e ignore a validação dos dados.
      - 🔄 Clique em "NEXT" e aguarde.

6. **Configurações de Dados:**
   - Configure as opções conforme indicado para File format, Delimiter, Encoding, etc.
   - 🔄 Clique em "NEXT".

7. **Configurações de Esquema:**
   - Não é necessário informar o caminho (path).
   - 🔄 Clique em "NEXT" e revise as configurações.

8. **Configurações de Tarefa:**
   - Em "Task settings":
      - Verifique as configurações e selecione os modelos desejados (por exemplo, RandomForest e LightGBM).
      - 💾 Clique em "SAVE".

9. **Configurações de Limites:**
   - Informe os valores para Max trials, Max concurrent trials, Max nodes, etc.
   - 🔄 Verifique as configurações e clique em "NEXT".

10. **Configurações de Computação:**
    - Em "COMPUTE", configure para Serverless, CPU, Dedicated, etc.
    - 🔄 Verifique as configurações e clique em "NEXT".

11. **Revisão e Submissão:**
    - Faça uma revisão final das configurações.
    - 🚀 Clique em "Submit training job" e aguarde o processo de treinamento (pode levar alguns minutos).

12. **Finalização:**
    - Após o treinamento, seu modelo estará pronto para uso.