# Justificativa
	
	Os arbovírus (ARthropod BOrne VIRUS) são vírus transmitidos por artrópodes (como os mosquitos hematófagos) que causam bastante preocupação em saúde pública, sendo os mais comuns no Brasil: Dengue (DNV), Zika (ZKV), Chikunguya (CHIKV) e Febre Amarela (YFV) (DONALISIO et al, 2017). Casos de Febre Amarela urbana não são reportados no Brasil desde 1942 (GOLDANI, 2017). No entanto, o YFV tem tido destaque na região pois somente no período de julho/2017 a Abril/2018 foram confirmados 446 casos de Febre Amarela do tipo Silvestre em Minas Gerais, sendo que 150 evoluíram para óbito conforme boletim de 04 de Abril da SES-MG (2018). Ainda que exista uma vacina segura e recomendada existem vários fatores que permitem que a doença ressurja periodicamente na África e Américas (JULANDER, 2013; GOLDANI, 2017). 
	
	Apesar de apresentar forma transmissão bastante distinta, o vírus da hepatite C (HCV) é da mesma família (flaviridae) dos arbovírus mencionados e apresenta ciclo de vida semelhante dentro da célula do hospedeiro humano infectado (GARDNER e RYMAN, 2010; AFZAL et al, 2015). Guo et al (2016) comentam sobre os medicamentos antivirais de ação direta (Direct Acting Antiviral, DAA), que são moléculas pequenas que agem diretamente no encapsulamento dos vírus, e ainda reforçam a importância de estudar medicamentos antivirais para os casos não resolvidos pela vacina. A partir de resultados positivos da ação de DAAs sobre o vírus da hepatite C (IOANNOU et al, 2017; VACHON e DIETERICH, 2017; KOIZUMI et al, 2017; CHATTERJEE et al, 2013), modelos in vitro e in vivo de YFV estão sendo utilizados para testar eficácia de DAAs sobre o vírus da Febre Amarela (GUO et al, 2016; JULANDER, 2013). 
	
	A proponente do presente projeto de Iniciação Científica tem formação de doutorado interdisciplinar em Modelagem Computacional com aplicação para a área de saúde, com tese intitulada “Acoplamento de Modelos Computacionais de Doenças Infecciosas” (Quintela, 2015). Durante o desenvolvimento da tese, propôs melhoria em um modelo matemático de equações diferenciais ordinárias e parciais baseado em idade para infecção e tratamento do vírus da hepatite C (HCV) com identificação de eficácia de DAAs que agem impedindo a replicação do RNA viral dentro das células sob orientação de Alan Perelson no Los Alamos National Laboratory (LANL). Outro modelo matemático que propôs na tese utilizou equações diferenciais parciais para representar difusão de antígenos (s. aureus) e células da resposta inata no tecido pulmonar, migração de célula apresentadora para ativação da resposta adquirida em um linfonodo, com produção de anticorpos, representada por equações diferenciais ordinárias. Este modelo está sendo adaptado pelo Center for Research and Education on Aging (CREA), University of California Berkeley, em pesquisa para entender melhor as relações da resposta imune no envelhecimento, em colaboração com a proponente. 
  
# Objetivo

	O objetivo geral do presente projeto de pesquisa é aplicar o conhecimento de desenvolvimento de sistemas para atender demandas das áreas de saúde. Para atingir tal objetivo propõe-se como objetivos específicos:
	
i. Desenvolvimento de uma ferramenta que utilize técnicas de mineração de dados e aprendizado de máquina para realizar previsões de ocorrência de futuros surtos de doenças. Espera-se coletar dados epidemiológicos e climáticos das regiões onde ocorreram surtos de doenças transmissíveis por mosquitos. Os dados coletados durante o tempo de duração do presente projeto serão utilizados para treinar e testar o modelo preditivo para que este possa ser utilizado para realizar previsões a partir de novos dados disponíveis.

ii. Estudo e implementação de um modelo matemático epidemiológico do YFV baseado nos trabalhos de Raimundo et al (2015) e Ribeiro et al (2015). Espera-se utilizar um modelo matemático epidemiológico de equações diferenciais ordinárias para geração de insights sobre formas de prevenção de surtos e para analisar, por exemplo, o impacto da vacinação e, evolução temporal das epidemias, considerando os dados disponíveis para a região de Juiz de Fora.

iii. Utilizar o modelo matemático já desenvolvido para testar eficácia de medicamentos de ação direta para tratamento do HCV (Quintela et al, 2018) para identificar a eficácia de medicamentos de ação direta para tratamento do YFV, baseado em dados disponibilizados nos trabalhos de Guo et al (2016) e Julander (2013). Esse tipo de modelo auxilia na compreensão do modo de ação do vírus e permite simulações de vários cenários que são impossíveis de testar in vivo em humanos além de reduzir a necessidade de modelos animais. Utilizado em conjunto com outros experimentos pode gerar insights para ajudar a direcionar experimentos in vitro e in vivo. 

# Metodologia
	A Epidemiologia é uma disciplina científica quantitativa baseada em dados e métodos bem estabelecidos para análises de dados relacionados à saúde pública (CDC, 2012). Uma ferramenta que tem sido bastante aplicada a Epidemiologia é a modelagem matemática (NOKES; ANDERSON, 1988; HUPPERT; KATRIEL, 2013). 
	
	Em Murray (2002) são apresentados vários exemplos de modelos matemáticos que incorporam aspectos da epidemiologia como transmissão de doenças, evolução temporal de epidemias, resistência a infecção adquirida, estratégias de vacinação, entre outros. 
	
	Devido à complexidade e multiplicidade de fatores envolvidos a epidemiologia tem se beneficiado também de tecnologias para permitir a análises de grandes bases de dados como mineração de dados e aprendizado de máquina (LYNCH e MOORE, 2016). 
	
	Para o desenvolvimento do modelo preditivo propõe-se a utilização de uma ferramenta gratuita, chamada WEKA, Waikato Environment for Knowledge Analysis (WITTEN et al, 2016). O projeto seguirá as seguintes etapas: análise dos dados disponíveis e pré-processamento conforme necessário; separação dos dados em conjuntos de treinamento e testes na proporção de (70/30); definição e desenvolvimento de um modelo de previsão; treinamento do modelo com vários algoritmos de aprendizado de máquina distintos disponíveis na ferramenta; testes; comparação dos resultados e escolha do algoritmo que apresente melhor desempenho para o conjunto de dados utilizado. 
	
	Para o modelo matemático de epidemiologia espera-se implementar as equações diferenciais ordinárias utilizando Matlab® (MATLAB, 2015), devido a familiaridade dos alunos da instituição e professora proponente do projeto e por possuir funções disponíveis para resolver esse tipo de sistema de equações e visualização dos resultados. Com relação aos métodos numéricos para resolução das equações serão utilizados métodos estabelecidos dando preferência a bibliotecas otimizadas. No caso do Matlab® para sistemas de EDOs espera-se utilizar a função ode45() para resolução do sistema de equações. Antes de ser implementado, o modelo matemático será analisado quanto a estabilidade e existência de solução. O solver será implementado de forma a facilitar a análise de sensibilidade do modelo aos parâmetros e ajuste de parâmetros.
	
	 O modelo multiscala baseado em idade de infecção e tratamento já possui um solver para equações diferenciais ordinárias e parciais implementado em Matlab®. O desenvolvimento de um solver em C/C++ para esse tipo de modelo está em andamento, no entanto, não ficará pronto a tempo do presente projeto. Para esse modelo, será utilizado o Matlab® para inserir as equações, realizar análise de sensibilidade aos parâmetros e realizar o ajuste dos parâmetros a partir de dados disponibilizados pela colaboração com projeto da UFJF, de pacientes infectados com YFV e tratados com antivirais.

# Referências 

AFZAL, M. S. et al. Regulation of core expression during the hepatitis C virus life cycle. Journal of General Virology, Microbiology Society, 96, 311-321. 2015. https://doi.org/10.1099/vir.0.070433-0. 

CDC, Centers for Disease Control and Prevention. Principles of Epidemiology in Public Health Practice. U.S. Department of Health and Human Services, 2012.

CHATTERJEE, A. et al. Hepatitis C Viral Kinetics. Clinics in Liver Disease, 17, no. 1 (February): 13–26, 2013. https://doi.org/10.1016/j.cld.2012.09.003 

DONALISIO, MR et al. Arboviruses emerging in Brazil: challenges for clinic and implications for public health. Revista de Saúde Publica, 51-30, 2017. 

GARDNER, C. L.; RYMAN, K. D. Yellow Fever: A Reemerging Threat. Clin Lab Med, 30(1), 237-60, 2010. 

GOLDANI, L. Z. Yellow fever outbreak in Brazil. The Brazilian Journal of Infectious Diseases. 21, 123-124, 2017.

GUO, F. et al. A Novel Benzodiazepine Compound Inhibits Yellow Fever Virus Infection by Specifically Targeting NS4B Protein. Journal of Virology, 90, 2016. 

HUPPERT, A.; KATRIEL, G. Mathematical Modelling and Prediction in Infectious Disease Epidemiology. Clinical Microbiology and Infection, 19, no. 11:999–1005. 2013. https://doi.org/10.1111/1469-0691.12308.

IOANNOU, George N. et al. HCV Eradication Induced by Direct-Acting Antiviral Agents Reduces the Risk of Hepatocellular Carcinoma. Journal of Hepatology, 68, no. 1 (January): 25–32, 2017.

JULANDER, J. G. Experimental therapies for yellow fever. Antiviral Research, 97, 169-79, 2013.

KOIZUMI, Yoshiki et al. Quantifying Antiviral Activity Optimizes Drug Combinations against Hepatitis C Virus Infection. Proceedings of the National Academy of Sciences,114, no. 8 (February 2017): 1922–1927. https://doi.org/10.1073/pnas.1610197114.

LYNCH, S. M.; MOORE, J. H. A call for biological data mining approaches in epidemiology. BioData Mining, 9:1, 2016.

MATLAB and Statistics Toolbox Release 2015a, The MathWorks, Inc., Natick, Massachusetts, United States, 2015.

MURRAY, J. D. Mathematical Biology. I. An Introduction. Vol. I. Springer, 2002.

NOKES, D. J.; ANDERSON, R. M. The Use of Mathematical Models in the Epidemiological Study of Infectious Diseases and in the Design of Mass Immunization Programmes. Epidemiology and Infection 101, no. 01:1–20. 2010. https://doi.org/10.1017/S0950268800029186.

QUINTELA, B M. Acoplamento de Modelos Computacionais de Doenças Infecciosas. Tese (Doutorado). Programa de Pós-graduação em Modelagem Computacional, Universidade Federal de Juiz de Fora. 2015.

QUINTELA, B. M. et al. A New Age-Structured Multiscale Model of the Hepatitis C Virus Life-Cycle During Infection and Therapy With Direct-Acting Antiviral Agents. Frontiers in Microbiology, 9, 601, 2018. https://doi.org/10.3389/fmicb.2018.00601 

RAIMUNDO, S. M. et al. Equilibrium Analysis of a Yellow Fever Dynamical Model with Vaccination. Computational and Mathematical Methods in Medicine, 2015. https://doi.org/10.1155/2015/482091 

REIS, Alessandro. Estudo de ferramentas baseadas no Weka para mineração de dados distribuída em ambiente de Grid. Monografia (Graduação) – Ciência da Computação, Universidade Federal de Lavras. 2012, 68.

RIBEIRO, A. F. et al. A Public Health Risk Assessment for Yellow Fever Vaccination: A Model Exemplified by an Outbreak in the State of São Paulo, Brazil. Memórias Do Instituto Oswaldo Cruz, 110, no. 2, 230–234. 2015. https://doi.org/10.1590/0074-02760140345.

SES-MG. Boletim epidemiológico - 03/04/2018 Febre Amarela Silvestre em Minas Gerais, 2018.

SHETTY, S.D. et al. Weka Based Desktop Data Mining as Web Service. World Academy of Science, Engineering and Technology. 4, no. 4 (2010): 19. rn:dai:10.1999/1307-6892/6914

VACHON, Marie-Louise; DIETERICH, D. T. The Era of Direct-Acting Antivirals Has Begun: The Beginning of the End for HCV?. Seminars in Liver Disease, 31, no. 4. 399–409, 2011.

WITTEN I.H. et al. Online Appendix on the WEKA Workbench. Data Mining: Practical Machine Learning Tools and Techniques, 4 ed. Morgan Kaufmann, 2016.




