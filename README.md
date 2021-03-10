# ISYANA_KBS
F. Mao, W.W. Weng, M. Pratama, E. Yapp Kien Yee Continual Learning via Inter-Task Synaptic Mapping, Knowledge Based Systems, 2021

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



## We develop from the source code: https://github.com/GMvandeVen/continual-learning
##The authors for that soruce code are (van de Ven, Gido M and Tolias, Andreas S)

#ISYANA work (ours) is based on the the source code above. 
Please consider citing our papers if you use our code in your research.



Manual for running the code:

##The dataset contains permMNIST, splitMNIST, rotMNIST and omniglot.

***Use main.py script to get results of ISYANA algorithm.  
"--epoch=N" is the parameter. The "N" can be set by yourself and this parameter means it runs N times with different random seeds each time. The command below means running 10 times.

1. splitMNIST

python main.py "--isyana" "--scenario=task" "--experiment=splitMNIST" "--tasks=5" "--fc-units=256" "--lr=0.01"  "--epoch=10" "--optimizer=sgd"


2. permMNIST

python main.py "--isyana" "--scenario=task" "--experiment=permMNIST" "--tasks=10" "--fc-units=500" "--epsilon=0.1"  "--lr=0.1"  "--epoch=10" "--optimizer=sgd"


3. rotMNIST

python main.py "--isyana"  "--scenario=task"  "--experiment=rotMNIST"  "--tasks=10"  "--fc-units=500"  "--epsilon=0.1"  "--lr=0.1", "--epoch=10"   "--optimizer=sgd"




***Use _compare.py script to get results of different algorithms including ISYANA algorithm. 


1. splitMNIST

python _compare.py  "--c=1" "--scenario=task" "--experiment=splitMNIST" "--tasks=5" "--fc-units=256" "--lr=0.01"  "--epoch=10" "--optimizer=sgd"


2. permMNIST

python _compare.py  "--c=1" "--scenario=task" "--experiment=permMNIST" "--tasks=10" "--fc-units=500" "--epsilon=0.1"  "--lr=0.1"  "--epoch=10" "--optimizer=sgd"



3. rotMNIST

python _compare.py "--c=1"  "--scenario=task"  "--experiment=rotMNIST"  "--tasks=10"  "--fc-units=500"  "--epsilon=0.1"  "--lr=0.1", "--epoch=10"   "--optimizer=sgd"



***Use drawIsyanaFigure.py to get the figure in the paper.
