# ISYANA_KBS
Continual Learning via Inter-Task Synaptic Mapping submitted to Knowledge Based Systems

Learning from streaming tasks leads a model to catastrophically erase unique
experiences it absorbs from previous episodes. While regularization techniques
such as LWF, SI, EWC have proven themselves as an effective avenue to over-
come this issue by constraining important parameters of old tasks from changing
when accepting new concepts, these approaches do not exploit common infor-
mation of each task which can be shared to existing neurons. As a result, they
do not scale well to large-scale problems since the parameter importance vari-
ables quickly explode. An Inter-Task Synaptic Mapping (ISYANA) is proposed
here to underpin knowledge retention for continual learning. ISYANA combines
task-to-neuron relationship as well as concept-to-concept relationship such that
it prevents a neuron to embrace distinct concepts while merely accepting rele-
vant concept. Numerical study in the benchmark continual learning problems
has been carried out followed by comparison against prominent continual learn-
ing algorithms. ISYANA exhibits competitive performance compared to state
of the arts.
