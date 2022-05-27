```
Introduction to Machine Learning

Learning: universal principles for living beings, society, machines

What is ML? 
• Learning: a complex aim, a continuously growing research field
• In Computer Science, theoretical and applicative field called:
	– Apprendimento Automatico in italiano (it)
	– Machine Learning (ML) English and literature (aka learning systems)
• Machine Learning has emerged as an area of research combining the aims of creating computers 
that could learn (IA) and new powerful adaptive/statistical tools with rigorous foundation 
in computational science
• Machines that learn by themselves. Why? Luxury or necessity?
	– Growing availability and need for analysis of empirical data
		→ Central/methodological role due to changing of paradigm in science: data-driven
	– Difficult to provide adaptivity/intelligence by programming [see Turing]
		→ learning as the only choice...
• DATA + HPC + modern ML → Pave the way to a new AI era

Aims include:
• As AI methodology → Build Adaptive Intelligent Systems
	– from search engine to robotics...
• As statistical learning
	→ Build powerful predictive system for Intelligent Data Analysis
	– tools for the “data scientist”
• As computer science method for innovative application areas
	→ Using models as a tool for complex (interdisciplinary) problems
	– from biological data analysis to image understanding...

Simple concrete examples
• Automatized learning by the system of the experience (set of examples) to address a computational task
	- Email spam classificaiton, character/face/speech recognition
• no (or poor) prior knowledge/rules for the solution but it is (more) easy 
to have a source of training experience (data with known results)
• Models used in Real-World systems (pervasive*) and in new interdisciplinary area, encompassing:
	– Pattern Recognition, Robotics, Computer Vision, Natural Language Processing,
	Information Retrieval, Web search engine, Complex Analyses of Data (Med, Bio, Web), 
	Data Mining, Financial forecasting, Adaptive Systems and Filters, Intelligent Sensor Networks 
	(Smart IoT), Personalized components...

An instance on a “recent” result (2014)
• Face recognition combining (deep) Neural Networks and other ML approaches
• Starting form four million facial images belonging to more than 4,000 identities
• Asked whether two photos show the same person, DeepFace answers correctly 97.25% of the time...
just a shade behind humans (97.53%).

Machine Learning: when? (summarizing)
Opportunity (if useful) and awareness (needs and limits)
• Utility of predictive learning models: (in the following cases)
	– no (or poor) theory (or knowledge to explain the phenomenon or difficult to be formalized)
	– uncertain, noisy or incomplete data (which hinder formalization of solutions)
	– dynamical environments, not known in advance (E.g. adapt to personalized behavior 
	according to dynamical user preferences)
• Requests:
	- source of training experience (representative data)
	- tolerance on the precision of results *

Machine Learning: why?
• An opportunity to know new computing paradigms, with an approach different 
w.r.t. to Standard Programming, algorithmic/classic IA approaches
	– e.g. treatment of uncertainty, tolerance of imprecision...
• Typical of the soft computing/computational intelligence area
• To find approximate solutions for difficult problems, difficult to be formalized by ‘hand-made’ algorithm
• To build new robust and wide applicable intelligent systems
• But it is NOT an approximate methodology!
• It is a rigorous approach to find approximate function to deal with complex problems 
(supported by empirical and theoretical results e.g. SLT),
	– soft computing paradigm: open many new opportunities (extend the frontier of CS applications)
	– Often bio-inspired (neural) modeling

Overview of a ML System:
	[Img. 10-1]

Learning as an approximation of an unknown function from examples
Specific vision but widespread in ML. For us:
	▪ Different tasks seen in uniform framework
	▪ Enables a rigorous formulation
		→ Intro guided by an intuitive example

An Example
• A pilot example: recognition of handwritten digits
• Input: collection of images of handwritten digits (arrays/matrix of values)
• Problem: build model that receives in input an image of handwritten digit and "predict" the digits
	- Classification problem
• Difficult to formalize exactly the solution of the problem: possible presence of noise and ambiguous data;
• Relatively easy to collect collection of labeled examples
	=> Example of successful application of the ML!

A step ahead from the pilot example
Generalizing the pilot example problem:
• Supervised learning (classification, regression)
	x (Input space vectors) -> (f, function built from examples) -> Categories or real values (R)

Tasks: Supervised Learning
• Given: Training examples as <input, output> = <x, d> (labeled examples)
for an unknown function f (known only at the given points of example)
	– Target value: desiderate value d or t or y... is given by the teacher according to f(x).
• Find: A good approximation to f (a hypothesis h that can used for prediction on unseen data x')
• Target d (or t or y): a categorical or numerical label
	– CLASSIFICATION: f(x) return the (assumed) correct class for x
		f(x) is a discrete-valued function ∈ {1, 2, ..., k} classes
	– REGRESSION: approximate a real-valued target function (in R or R^K)
Both as a function approximation task

Examples of x - f(x)
Inferring general functions from know data:
• Handwriting Recognition
	– x: Data from images of the characters.
	– f(x): Letter of the alphabet.
• Disease diagnosis (from database of past medical records)
	– x : Properties of patient (symptoms, lab tests)
	– f(x): Disease (or maybe, recommended therapy)
	– TR (training set) <x, f(x)>: database of past medical records
• Face recognition
	– x: Bitmap picture of person's face
	– f(x): Name of the person.
• Spam Detection
	– x: Email message
	– f(x): Spam or not spam.

Tasks: Unsupervised Learning
Unsupervised Learning: No teacher!
• TR (Training Set) = set of unlabeled data <x>
• E.g. to find natural groupings in a set of data
	– Clustering
	– Dimensionality reduction/Visualization/Preprocessing
	– Modeling the data density

• Clustering: Partition of data into clusters (subsets of “similar” data)
	[Img. 10-2]

Models and survey of useful concepts
• MODEL:
	– Aim: to capture/describes the relationships among the data (on the basis of the task)
	– It defines the class of functions that the learning machine can implement (hypothesis space)
		• E.g. set of functions h(x, w), where w is the (abstract) parameter
• Training example (superv.): An example of the form (x, f(x) + noise)
	x is usually a vector of features, (d or t or) y = f(x) + noise is called the target value
• Target function: The true function f
• Hypothesis: A proposed function h believed to be similar to f.
An expression in a given language that describes the relationships among data
• Hypotheses space: The space of all hypotheses (specific models) 
that can, in principle be output by the learning algorithm

Models Languages for H
• alcuni linguaggi in cui esprimere relazioni che possiamo usare per esprimere modelli di ML (le ipotesi h):
	- Logica del primo ordine
	- Equazioni numeriche
	- Probabilità: questo verrà reintrodotto per la rappresentazione della conoscenza incerta in AI 
	(e quindi per esprimere modelli di ML)

Models: few simple examples...
Just to have a preview of different representation of hypothesis:

• Linear models (representation of H defines a continuously parameterized space of potential hypothesis);
each assignment of w is a different hypothesis, e.g:
	- hw(x) = w1x + w0 
	E.g. hw(x) = 0.232x + 246

• Symbolic Rules: (hypothesis space is based on discrete representations);
different rules are possible, e.g: 
	– if (x1 == 0) and (x2 == 1) then h(x) = 1
	– else h(x)= 0

• Probabilistic models: estimate p(x, y)
• Instance based approaches: Predict mean y value of nearest neighbors (memory-based)

Learning Algorithms
• LEARNING ALGORITHM
• Basing on data, task and model, learning as a (Heuristic) search through the hypothesis space H 
of the best hypothesis = the best approximation to the (unknown) target function.
	– i.e. the best approximation to the (unknown) target function
• Typically searching for the h with the minimum “error”
• E.g. free parameters of the model are fitted to the task at hand:
	– Examples: best w in linear models, best rules for symbolic models, ...
• H may not coincide with the set of all possible functions and the search can not be exhaustive: 
it needs to make assumptions → we will see the role of the Inductive bias

Machine Learning: generalization
• Learning: search for a good function in a function space from known data 
(typically minimizing an Error/Loss)
• Good w.r.t. generalization error: it measures how accurately the model predicts 
over novel samples of data (Error/Loss measured over new data) (low error, high accuracy and vice versa)

Generalization: crucial point of ML!!! Easy to use ML tools versus correct/good use of ML

Generalization
• Learning phase (training, fitting): build the model from know data – training data (and bias)

• Predictive phase (test): apply to new example (we take the input x; we compute the response by the model;
we compare with its target that the model has never seen): evaluation of the predictive hypothesis, 
i.e. of the generalization capability

Note: performance in ML = predictive accuracy 
	-> estimated by the error computed on the (Hold out) Test Set
• Theory: E.g. Statistical Learning Theory [Vapnik]:
	– under what (mathematical) conditions is a model able to generalize? 

Concept Learning

Overview
• Concept Learning from examples as research in the Hypothesis Space
	– an opportunity to have a look of a simple symbolic learning system (propositional) (rule based)
	– as the basis for the subsequent introduction of flexible models
• Discrete space (symbolic representation of the target function), structure of the hypothesis space
• Representation: examples: Conjunction of literals
• Search Alg.: Find-S, candidate elimination
• Inductive Bias

Learning Problem
• Learning as Improving with experience at some task
• Improve over task T, with respect to performance measure P, based on experience E.

Supervised learning
• Given: Training examples as <input, output> = <x, d>
for an unknown function f (known only at the given points of example)
	– Target value: desiderate value d or t or y... is given by the teacher according to f(x).
• Find: A good approximation to f (a hypothesis h that can used for prediction on unseen data x’)
• Target d (or y or t): a categorical or numerical label
	– Classification: f(x) returns the (assumed) correct class for x 
				-> f(x) is a discrete-valued function
	– Regression: approximate a real-valued target function (in R o R^K)
Both as a task in function approximation

Now we see: CLASSIFICATION

Concept Learning
• Concept Learning: inferring a Boolean function from positive and negative training examples
• C: X → {t,f} or {+,-} or {yes, no} or {0,1}, X: instance space
• Examples of concepts: category “cat” or “enjoy-sport”

• Def: “Example”: <x, c(x)> in D (o TR set)
• Def: h: X → {0, 1} satisfies x if h(x) = 1
• Def: a hypothesis h is consistent with
	– An example <x, c(x)>, x in X, if h(x) =c (x)
	– D, if h(x) = c(x) for each training example <x, c(x)> in D.

An example:
Learning Boolean functions

This is an ill posed (inverse) problem:
We may violate either existence, uniqueness, stability of the solution or solutions

• There are 2^16 = 2^(2^4) = 65536 possible Boolean functions over four input features. 
We can't figure out which one is correct until we've seen every possible input-output pair.
• After 7 examples, we still have 2^9 (512) possibilities.
• In the general case: |H| = 2^(#instances) = 2^(2^n) for binary inputs/outputs, n = input dimension

Guide to next solutions
• Work with a restricted hypothesis space: we start choosing a space of hypotheses H 
that is considerably smaller than the space of all possible functions! (language bias)
• We will see:
	- (Simple) conjunctive rules (in a finite discrete H)
	- Linear functions (in an infinite continuous H)

• How to organize and efficiently search through a (discrete) space of hypothesis: 
some algorithms for a very restricted set of hypotheses
	– Conjunctive rules
	– No noisy data

Conjunctive Rules
• How many distinct h? = How many simple conjunctive rules?
	– 4 inputs: True, 4 single, 6 couple, 4 triple, 1 quadruple: 16
• In the general case:
	- Positive literals, e.g.: h1 = l2, h2 = (l1 and l2), h3 = true...
		–> Simple conjunctive rules
		–> |H| = 2^n (image li as a bit of a string of length n)
	- Literals (also not(li))
		–> |H| = 3^n + 1 (why?)

Representing Hypothesis
• Hypothesis h is a conjunction of constraints on attributes
• Each constraint can be:
	– A specific value: e.g. Water=Warm
		– A don’t care value : e.g. Water=?
	– No value allowed (null hypothesis): e.g. Water=Ø (e.g. li AND not(li))
• Example: hypothesis h (h in the following)
	Sky Temp Humid Wind Water Forecast
	< Sunny ? ? Strong ? Same>
Corresponding to boolean function:
	Sky=Sunny ∧ (and) Wind=Strong ∧ (and) Forecast=Same

< Ø Ø Ø Ø Ø Ø > Most specific
< ? ? ? ? ? ? > Most general

Prototypical Concept Learning Task
Given:
• Instances X: Possible days decribed by the attributes Sky, Temp, Humidity, Wind, Water, Forecast
• Target function c: EnjoySport X → {0,1}
• Hypotheses H: conjunction of (a finite set of) literals e.g.
	< Sunny ? ? Strong ? Same >
• Training examples D : positive and negative examples of the target function: 
	<x1, c(x1)>, ..., <xn, c(xl)>
Find:
• A hypothesis h in H such that h(x)=c(x) for all x in X.

Learning: searching in the hypotheses space H

Inductive Learning Hypothesis
• Assumption here: ”Any hypothesis found to approximate the target function well over the training examples,
will also approximate the target function well over the unobserved examples”.
• h(x)=c(x) for all x in D (i.e. consistent with D)
• h(x)=c(x) for all x in X (?)
• (?) = I.e. The Foundamental issue of the ML:
	– theoretical and empirical analysis

Number of Instances, Concepts, Hypotheses
Esempio:
– Sky: Sunny, Cloudy, Rainy (3 values!)
– AirTemp: Warm, Cold
– Humidity: Normal, High
– Wind: Strong, Weak
– Water: Warm, Cold
– Forecast: Same, Change
• The representation chosen for H determines the search space

#distinct instances: 3*2*2*2*2*2 = 96
#distinct concepts: 2^96 = 2^(#instances)
#syntactically distinct hypotheses (conjunctions): 5*4*4*4*4*4=5120
#semantically distinct hypotheses: 1+4*3*3*3*3*3=973
(because all h with Ø are equivalen to "false")

In general: high dimension, even infinite: 
structuring the search space may help in searching more efficiently

General to Specific Ordering
• Consider two hypotheses:
	– h1 = <Sunny,?,?,Strong,?,?>
	– h2 = <Sunny,?,?,?,?,?>
• Set of instances covered by h1 and h2:
	h2 imposes fewer constraints than h1 and therefore classifies more instances x as positive 
	[i.e. h(x)=1].

Def: Let hj and hk be boolean-valued functions defined over X. 
Then hj is more general than or equal to hk (written hj >= hk) if and only if
	Per ogni x appartenente a X : [(hk(x) = 1) → (hj(x) = 1)]
Examples over binary:
	- li: l1 >= (l1 and l2)
	- l1 versus l2: not comparable
• The relation >= imposes a partial order (p.o.) over the hypothesis space H 
that is utilized by many concept learning methods.
• We can take advantage of this p.o. to efficently organize the search in H

Find-S Algorithm
Exploit m.g.t. partial order to efficiently search consistent h (without explicitly enumerating every h in H)

1. Initialize h to the most specific hypothesis in H
2. For each positive training instance x
	For each attribute ai in h
	If the ai in h is satisfied by x 
		then do nothing
	else replace ai in h by the next more general constraint that is satisfied by x 
	[e.g. remove from h literals not satisfying x]
3. Output hypothesis h

Properties of Find-S
• Hypothesis space described by conjunctions of attributes (hard limitations!)
• Find-S will output the most specific hypothesis within H
that is consistent with the positive training examples
• The output hypothesis h will also be consistent with the negative examples, 
provided the target concept is contained in H.
– Because c >= h

Complaints about Find-S
• Can’t tell if the learner has converged to the target concept, in the sense that it is unable 
to determine whether it has found the only hypothesis consistent with the training examples.
• Can’t tell when training data is inconsistent, as it ignores negative training examples: 
no noise tollerance!
• Why prefer the most specific hypothesis?
• What if there are multiple maximally specific hypothesis?

Version Spaces
Key idea: ouput a description of the set of all h consistent with D
We can do it without enumerating them all
• Consistent(h,D) := Per ogni <x,c(x)> appartenente a D, h(x)=c(x)
• The version space, VS_H,D, with respect to hypothesis space H and training set D, 
is the subset of hypotheses from H consistent with all training examples:
VSH,D = {h appartenente a H | Consistent(h,D)}

List-Then Eliminate Algorithm
1. VersionSpace a list containing every hypothesis in H
2. For each training example <x,c(x)>
remove from VersionSpace any hypothesis that is inconsistent
with the training example h(x) != c(x)
3. Output the list of hypotheses in VersionSpace
Irrealistic: exuastive enumeration of all h in H

Representing Version Spaces [Img. 11-1]
• The general boundary, G, of version space VS_H,D is the set of maximally general members 
(of H consistent with D).
• The specific boundary, S, of version space VS_H,D is the set of maximally specific members 
(of H consistent with D).
• Theorem: Every member of the version space lies between these boundaries
	VS_H,D = {h appartenente a H| (Esiste s appartenente a S) (Esiste g appartenente a G) 
		(g >= h >= s)
	where x >= y means x is more general or equal than y

We can make a complete search of consistent hypotheses using the two boundaries S and G for the VS,
i.e. not restricted to S as for Find-S.

Candidate Elimination Algorithm
G <- maximally general hypotheses in H
S <- maximally specific hypotheses in H

For each training example d=<x,c(x)>:
If d is a positive example:
	Remove from G any hypothesis that is inconsistent with d (def. of VS)
	For each hypothesis s in S that is not consistent with d [generalize S]:
		• remove s from S.
		• Add to S all minimal generalizations h of s such that
			– h consistent with d
			– Some member of G is more general than h (<-*)
		• Remove from S any hypothesis that is more general than another hypothesis in S
If d is a negative example:
	Remove from S any hypothesis that is inconsistent* with d [*h is 1]
	For each hypothesis g in G that is not consistent with d [specialize G]:
		• remove g from G.
		• Add to G all minimal specializations h of g such that
			– h consistent with d
			– Some member of S is more specific than h (<-* key point in the example later)
• Remove from G any hypothesis that is less general than another hypothesis in G

Esempio Candidate Elimination: [Img. 11-2]

Inductive Bias and its role

• Our hypothesis space is unable to represent a simple disjunctive target concept: 
	(Sky=Sunny) v (Sky=Cloudy)
x1 = <Sunny Warm Normal Strong Cool Change> +
x2 = <Cloudy Warm Normal Strong Cool Change> +
	S: {<?, Warm, Normal, Strong, Cool, Change>}
x3 = <Rainy, Warm, Normal, Strong, Cool, Change> -
	S: {}
Bias: We assume that the hypothesis space H contain the target concept c.
In other words that c can be described by a conjunction (by AND operator) of literals.

Unbiased Learner
• Idea: Choose H that expresses every teachable concept, 
that means H is the set of all possible subsets of X: the power set P(X)
• |X|=96, |P(X)|=2^96 ~ 10^28 distinct concepts
• H = disjunctions, conjunctions, negations
	– e.g. <Sunny Warm Normal ? ? ?> v <? ? ? ? ? Change>
• H surely contains the target concept.
• What for generalitazion?

What are S and G in this case?
Assume positive examples (x1, x2, x3) andnegative examples (x4, x5)
S: {(x1 v x2 v x3)} 
G: {not(x4 v x5)}
The only examples that are unambiguolsy classified are the training examples themselves 
(H can represent them).
In other words in order to learn the target concept one would have to present 
every single instance in X as a training example.
Property: An unbiased learner is unable to generalize.
Proof: Each unobserved instance will be classified positive by precisely half the hypothesis in VS 
and negative by the other half (rejection).
Indeed:
Per ogni h consistent with xi (test), Esiste h’ identical to h except h'(xi) <> h(xi),
h appartiene a VS -> h' appartiene a VS (they are identical on D)

Futility of Bias-Free Learning
• A learner that makes no prior assumptions regarding the identity of the target concept 
has no rational basis for classifying any unseen instances.
• (Restriction, preference) bias not only assumed for efficiency, it is needed for generalization
	– However, does no tell us (quantify) which one is the best solution for generalization
• Trivial Example (TR = Training Set, TS = Test Set):
	X c(x)		H={x, not(x), 0, 1}
	TR 0 0 		VS={x,0}
	TS 1 ? 		→ Can be 1 or 0... Unless you use all X as TR set.
• Issue: characterize the bias for different learning approaches 

Inductive Bias
Consider:
• Concept learning algorithm L
• Instances X, target concept c
• Training examples D_c={<x,c(x)>}
• Let L(xi,D_c) denote the classification assigned to instance xi by L after training on D_c

Definition:
The inductive bias of L is any minimal set of assertions B such that:
for any target concept c and corresponding training data D_c:
	(Per ogni xi appartenente a X)[B && D_c && xi] |— L(xi, D_c)
Where A |— B means that A logically entails B (follows deductively from). 

Inductive Systems and Equivalent Deductive Systems:
	[Img. 11-3]

Three Learners with Different Biases
• Rote learner (lookup table): Store examples, classify x if and only if 
it matches a previously observed example.
	– No inductive bias -> no generalization
• Version space candidate elimination algorithm.
	– Bias: The hypothesis space contains the target concept (conj. of attributes) 
		|H|= 973 versus 10^28
• Find-S
	– Bias: The hypothesis space contains the target concept 
	and all instances are negative instances unless the opposite is entailed by its other knowledge 
	(seen as positive examples).
	– In other words: we have a language bias due to the AND on the literals 
	plus the search bias due to the preference of the most specific hyphotesis

Other symbolic - rule based approaches
Overcome the conjunctive restriction toward flexible models:
Many approaches in ML, e.g.:
• Decision trees
• Genetic Algorithms:
	– encode each rule set as a bit string and uses genetic search operator to explore this H
• Inductive Logic Programming:
	– First-order logic rules that contain variables (much more expressive than propositional rules)
	– Automatic inferring Prolog programs from examples (collection of Horn clauses)

Linear models

Sintesi (ingredienti)
• Dati di Allenamento
• Spazio delle Ipotesi H,
	– costituisce l’insieme delle funzioni che possono essere realizzate dal sistema di apprendimento;
	– si assume che la funzione da apprendere f possa essere rappresentata da una ipotesi h in H
	(selezione di h attraverso i dati di apprendimento)
	– o che almeno una ipotesi h in H sia simile a f (approssimazione);
• Algoritmo di Ricerca nello Spazio delle Ipotesi, alg. di apprendimento
	– E.g. Adattamento dei parametri liberi del modello al task
• NOTA: H non può coincidere con l’insieme di tutte le funzioni possibili e la ricerca essere esaustiva 
		-> Bias Induttivo

Regression
Tasks: regression
• Process of estimating of a real-value function on the basis of finite set of noisy samples
	– known pairs(x , f(x) + random noise)

Linear models
• How to use the model
• Build (learn) the model (a simple regression model)
	- i.e how to find the w values of the linear model in a «systematic» way

Univariate Linear Regression
• Univariate case, simple linear regression:
	- We start with 1 input variable x, 1 output variable y
	- We assume a model h_w(x) expressed as out = w1x + w0
		-> where w are real-valued coefficients/free parameters (weights)
	- Fitting the data by a “straight line”

Task and Model (an example)
• Find h (linear model) that best fit data (from observed data set of x and y values)
• Assuming that the given variable (y) is (linearly) related to another variable (x) or variables 
by y = w1x + w0 + noise, where w are the free par. and noise is the error in measuring the targets 
(with normal distribution)
• we build a model (finding w values) to predict/estimate the price (y) 
of points for other (unobserved) x values

Use it (as ML predictive tool)!
• Predict/estimate the price (y) of points for other (unobserved) x values

Build it: Learning via LMS (premise)
• We have to find the values of the parameters w (w1 and w0 in the univariate case) 
in order to minimize the model output error (to make a good fitting)
• Infinite hypthiesis space (continuous w values) but we have nice solution from classical math 
	– Surprisingly we can “learn” by this basic tool
	– Although simple it includes many relevant concept of modern ML 
	and it is a basis of evoluted methods in the field
• Let us define a loss/error function and use the Least Mean Square (LMS) approach

Build it: Learning via LMS 
• Learn → find w such that minimize error/empirical loss 
(best data fitting – on the training set with l examples)
• Given a set of l training examples (xp, yp) p = 1...l
• Find: h_w(x) in the form w1x + w0 (hence the values of w) 
that minimizes the expected loss on the training data.
• For the loss we use the square of errors:
	- Least (Mean) Square: Find w to minimize the residual sum of squares [argminw Error(w) in L_2]:
		[Img. 12-1]

Why LMS to find the best h?
	[Img. 12-2]
• The method of least squares is a standard approach to the approximate solution of over-determined systems,
i.e., sets of equations in which there are more equations than unknowns. 

How to solve?
	[Img. 12-3]

Spazi continui - gradient
• Se la f è continua e differenziabile, e.g. quadratica rispetto ad x
• Il minimo o massimo si può cercare utilizzando il gradiente, 
che restituisce la direzione di massima pendenza nel punto
• Hill climbing iterativo: quantifica lo spostamento, senza cercarlo tra gli infiniti possibili successori

Nota generale: non sempre è necessario il min/max assoluto: caso del ML

Gradient descent (local search)
• iterative algorithm
• Gradient = ascent direction: we can move toward the minimum with a gradient descent 
		(Deltaw= - gradient of E(w))
-> Local search: begins with initial weight vector. 
Modifies it iteratively to decrease up to minimize the error function (steepest descent)

w_new = w + eta * Deltaw 
Where eta is a constant (step size), called learning rate

Gradient descent: intuitive motivations
• This is an “error correction” rule (call it delta rule) 
that changes the w proportionally to the error (target-output): 
	– (target y – output) = err = 0 -> no correction
	– output > target -> (y - h) < 0 (output is too high)
		-> Deltaw0 negative → reduce w0 and
		if (input x > 0) Deltaw1 negative -> reduce w1 
		else increase w1
	– output < target → (y - h) > 0 (output is too low)... [exercise]

Gradient descent: final discussion
Gradient descent approach is a simple and effective local search approach to LMS solution and:
	• it allows us to search through an infinite hypothesis space!
	• it can be easily always applied for continues H and differentiable loss: 
	NOT ONLY to linear models! (e.g. Neural Networks and deep learning models)
	• Efficient? Many improvement are possible, e.g. Newton's methods, Conjugate Gradient...

Linear models
• Extension to l data
• Extension to input vectors
• Summary of the LMS
• The gradient descent training algorithm

For l patterns:
	[Img. 12-4]
• We can update w after (repeating) an “epoch” of l training data -> Batch algorithm 
• Or we can update w after each pattern p → On-line algorithm (stochastic gradient descent)
	– it can be the faster, but needs smaller step

Multidimensional input (input vectors x): examples
• This is the standard case, using 2 up to hundreds of input variables/features:
	x = [x1, x2, ..., xn] (The input pattern is a vector)
• many possibilities in a wide range of applicative fields

• w0 is the intercept, threshold, bias, offset...

Geometrical view: hyperplane
	[Img. 12-5]

Summary: Input dimension n, l patterns
• Given a set of l training examples (xp, yp)
• Find: The weight vector w that minimizes the expected loss on the training data
	[Img. 12-6]

Summary: Gradient descent algorithm
A simple algorithm:
1) Start with weight vector w_initial (small), fix eta (0 < eta < 1).
2) Compute Deltaw= – “gradient of E(w)” (i.e. for each wi)
3) Compute w_new = w + eta*Deltaw 	(i.e. for each wi) 
where eta is the “step size” (learning rate) parameter
4) Repeat (2) until convergence or E(w) is "sufficiently small"

▪ Deltaw/l: least mean squares
• Batch versions (Deltaw after each “epoch” of l data): as previous slides
• Stochastic/on-line version: upgrade w for each pattern p (without waiting the total sum over l)
• eta -> learning rate: speed/stability trade-off, can be (gradually) decreased to zero 
(guarantees convergence, avoiding oscillation around the min.)

Advantages of linear models
• If it works well it is a “wonderful” model
	– Very simple
	– All the information on data is in w
	– Easy to be interpreted: everyday practice in medicine, biology, chemistry, economy...
	– Noisy data are allowed
	- Statisticians are happy (nice properties)
	- Linear phenomena -> a dream for science: ideal to make a “natural law”
• A baseline for learning (first: is it a linear problem?)
• It is used/included in more complex models

Linear models
• Limitations
• Linear Basis Expansion
• Regularization

Moving toward non-linear relationships
Note that in hw(x) = w1x + w0
• As Statistical Parametric models: "linear" does not refer to this straight line, 
but rather to the way in which the regression coefficients w occur in the regression equation
• Hence, we can use also transformed inputs, such are x, x^2, x^3, x^4...
with non-linear relationship inputs and output  holding the learning machinery 
(Least Square solution) developed so far

Example
• The result of fitting a quadratic function, M=2, through a set of data points.
• In linear least squares the function need not be linear in the argument (input variables) 
but only in the parameters (w) that are determined to give the best fit.

Generalization - LBE (shown for regression)
• Basis transformation -> linear basis expansion:
	[Img. 12-7]
• Augment the input vector with additional variables which are transformations of x 
according to a function phi (phi_k: R^n -> R)
• E.g.:
	– Polynomial representation of x: phi(x)=xj^2 or phi(x)= xjxi, or...
	– Non-linear transformation of single inputs: phi(x)=log(xj), phi(x)= root(xj)...
	– Non-linear transformation of multiple input: phi(x)= ||x||
	– Splines...
• Number parameters K > n (before it was n)
• The model is linear in the parameters (also in phi, not in x): 
we can use the same learning alg. as before!

Basis Expansion examples:
	[Img. 12-8]

Basis Expansion criticism
• Which phi? Toward the so called “dictionary” approaches
• PROS: 
	+ It is more expressive: it can model more complicated relationships (than linear).
• CONS: 
	- With large basis of functions, we require methods for controlling the complexity of the model

1st Order Polynomial (linear model): 
	- M = 1
	- too poor solution (underfitting)
3rd Order Polynomial: 
	- M = 3
	- more flexibility is useful!
9th Order Polynomial:
	- M = 9
	- excessive flexibility! E(w) = 0 on training data, but error on test set
	- too complex model: fit the noise
	- poor representation of the true function (overfitting)

Complexity tradeoff
• Too simple model:
	– Doesn’t fit the data well
	– Biased solution
	- UNDERFITTING
• Too complex model:
	– Highly sensitive to slight perturbations of the data
	– High variance solution (Bias-variance)
	- OVERFITTING
• Want to choose regularization to balance out bias and variance
	-> Trough control of model complexity (seen as flexibility)

Toward Regularization
• It can control overfitting by penalizing “complex” functions (large weights) 
(i.e. toward coefficient shrinkage) while maintain the flexibility of the hypothesis space
• Occam (Ockham) razor:
	“The simplest explanation is more likely the correct one” 
	or “prefer the simplest hypothesis that fits the data”
• This fundamental concept in ML will be found again and we will “rationalize” it at the end 
	– Whereas complexity is not for the computational cost 
	but a measure of the flexibility of the model to fit the data
• Now let us introduce an approach for linear models: regularization by ridge regression

Regularization by Ridge Regression
• Ridge regression/Tikhonov regularization: smoothed models
	– possible to add constraints to the sum of value of |wj| favouring "sparse" models 
	e.g. with less terms due to weights wj = 0 (or close to 0) (it means a less complex model)
Formula:
	[Img. 12-9]
– Effect: weight decay (basically add 2*Lambdaw to the gradient of the Loss)
E.g. with zero gradient, it decreases the value of each w with a fraction of the old w

Regularization by Ridge Regression: discussion
• General applicability (not only for polynomials)
	– e.g. we can control model complexity just using lambda, without not knowing M as for polynomials,
	or even when the model complexity is not known
• Note the balancing (trade-off) between the two terms:
	– Small error data term (minimize just the training error) is not enough for us: 
	we want also to control the complexity of the model to control the overfitting, 
	hence we introduce the second term in the minimization.
	– On the other side, we can exceed because to much weight to the second term (high lambda value)
	leads to focus the minimization only or mostly on the regularization, hence the data error 
	(first term) could grow too much, i.e. moving to underfitting
	– The trade-off is ruled by the value of lambda (regularization coefficient)

Too low lambda (lambda = 0) -> OVERFITTING
Too high lambda (lambda = 1) -> UNDERFITTING

Limitations of Fixed Basis Functions
• Having basis function along each dimension of a D-dim. input space 
requires combinatorial number of functions
	-> the curse of dimensionality
	▪ e.g. general polynomials of order 3 use all combination of input variables 
	due to products x1*x2, x2*x3, ..., x1*x2*x3 etc. -> D^3 (approximationas D increases)
• Phi are fixed before observing training data
	- In other models, we can get away with fewer basis functions, by choosing these 
	using the training data: phi (in a hidden computational layer) depends on w 
	and the model is not-linear in the parameters. E.g. Neural Networks
	- In other models the computation of the new embedding space (input transformation) 
	is made implicitly through kernel functions and controlling the complexity of the model. E.g. SVM

Linear model - Classification
We reuse the linear model
• The same models (used for regression) can be used for classification: 
categorical targets, e.g. 0/1 or -1/+1.
- In this case we use a hyperplane (wx) assuming negative or positive values
- We exploit such models to decide if a point x belongs to positive or negative zone of the hyperplane 
(to classify it)
- So we want to set w (by learning) so that we get good classification accuracy

Geometrical view: hyperplane and classifier
	[Img. 12-10, 12-11]

Classification by linear decision boundary
The classification may be viewed as the allocation of the input space in decision regions (e.g. 0/1)
Example: linear separator on 2-dim instance space x = (x1, x2) in R^2, f(x) = 0/1 (or -1/+1) 

h(x) = { 1 if wx + w0 >= 0	[0, 1] outputs
	 0 otherwise }
h(x) = sign(wx + w0)		[-1, +1] outputs
	-> Linear threshold unit (LTU)

Threshold (bias w0)
Note that, given the bias w0, in the LTU saying:
	h(x) = w^Tx + w0 >= 0 
is equivalent to saying:
	h(x) = w^Tx >= -w0
with –𝑤0 as the «threshold» value

• The two forms identify the same positive zone of the classifier
• The second one emphasizes the role of the bias as a threshold value 
to “activate” the +1 output of the classifier.

Use it: example
	[Img. 12-12]

Learning problem for linear classifiers: 
	[Img. 12-13]

DeltaW as Error Correction Learning rule
If misclassified (because target is +1) 
	-> High positive delta for w1 and w3 
		-> increase them proportionally (with eta) to the delta, 
	hence a positive value in this case [error correction rule]

Summarizing
• Model trained (on tr set) with LS (LMS) on wx 
by the simple gradient descent algorithm used for linear regression
• Model used for classification applying the threshold function h(x) = sign(wx)
• The error can be computed as classification error or number of misclassified patterns 
(not only by the Mean Square Error)
• ACCURACY = mean of correctly classified = (l-num_err)/l

Learning Algorithm
• The same as for regression: see “Gradient descent algorithm”
• Also the linear basis expansion and Tikhonov can be applied as well
• Note that (learning algorithm):
	– It converges asymptotically to the MinLS
	– Not necessarily to the min number of classification errors
• [If w are not changed for correct outputs (hw(xp) = dp) we obtain the update rule for the perceptron]

Example: Conjunctions
• We can represent conjunctions by the linear models, e.g.:
4 var: x1 && x2 && x4 <-> y
• 1 x1 + 1 x2 + 0 x3 + 1 x4 > 2
• 1 x1 + 1 x2 + 0 x3 + 1 x4 >= 2.5

2 var: x1 && x2 <-> y
• 1 x1 + 1 x2 > 1
• 1 x1 + 1 x2 >= 1.5

Limitations
• In geometry, two set of points in a two-dimensional plot are linearly separable 
when the two sets of points can be completely separated by a single line
• In general, two groups are linearly separable in n-dimensional space 
if they can be separated by an (n-1)-dimensional hyperplane.
• The linear decision boundary can provide exact solutions only for linearly separable sets of points

Non linear decision boundary: Examples
	[Img. 12-14]

Other learner models for classification
• Linear Discriminant Analysis (also multi-class)
• Logistic regression
	– P(y|x) starting from modeling the class density as a know density
	– Soft threshold (continuous, differentiable) with logistic function (instead of 0/1 hard threshold)
• Neural networks (NN) and SVM mentioned before: flexible models including non-linear approximation 
for both regression and classification.
	– NN use many units (similar to LTU) within different layers
	– Feature representation learning in each layer (deep learning concept)
	– Gradient descent approach for learning

Conclusions on Linear Models
• Basic well-founded approach for both regression and classification
	– Very compact way to represent knowledge
	– But with a strong assumption on the relationship among data
• An iterative error correction (LMS) algorithm that search continuous hypothesis spaces
	– (that is the basis for many other ML approaches)
• A view of limitations of linear approaches and of the needs for more flexible ML models and their issues:
	– An extension of linear model for non-linear tasks
	– An introduction to the control of complexity (regularization)

Introduction to Decision Trees Learning

Overcome the conjunctive restriction toward flexible models:
[in the class of symbolic - rule based approaches]
• Decision trees (a popular approach in ML/DM)

Decision trees: expressive power
• Decision trees represent a disjunction of conjunctions of constraints on the value of attributes:

(Outlook = Sunny || Humidity = Normal) ||
(Outlook = Overcast) ||
(Outlook = Rain && Wind = Weak)

Or if-then-else rules.
H of D.T. capable of expressing any finite discrete-valued function (propositional)

Top-down induction of Decision Trees
• ID3 is a basic algorithm for learning DT's
• Given a training set of examples, the algorithms for building DT 
performs search in the space of decision trees
• The construction of the tree is top-down. The algorithm performs a greedy search.
• The fundamental question is “which attribute should be tested next”? 
Which question gives us more information gain?”
• Select the best attribute
• A descendent node is then created for each possible value of this attribute 
and examples are partitioned according to this value
• The process is repeated for each successor node until all the examples 
are classified correctly or there are no attributes left

ID3: algorithm
ID3(X, T, Attrs) 
			X: training examples
			T: target attribute (e.g. PlayTennis)
			Attrs: other attributes, initially all attributes
Create Root node
If all X's are +, return Root with class +
If all X's are –, return Root with class –
If Attrs is empty return Root with class most common value of T in X
else
	A <- best attribute; decision attribute for Root <- A
	For each possible value vi of A:
		- add a new branch below Root, for test A = vi
		- Xi <- subset of X with A = vi
		- If (Xi is empty) then 
			add a new leaf with class the most common value of T in X
		else 
			add the subtree generated by ID3(Xi, T, Attrs − {A})
return Root

Selecting the best attribute: entropy
• We use the notion of entropy, commonly used in information theory
• Entropy measures the impurity of a collection of examples. 
It depends from the distribution of the random variable p.
	– S is a collection of training examples
	– p+ the proportion of positive examples in S
	– p– the proportion of negative examples in S

Entropy (S) = – p+ * log2(p+) – p– * log2(p–)	[assume 0 log2(0) = 0]

Entropy ([14+, 0–]) = – 14/14 log2(14/14) – 0 log2(0) = 0
Entropy ([9+, 5–]) = – 9/14 log2(9/14) – 5/14 log2(5/14) = 0,94
Entropy ([7+, 7– ]) = – 7/14 log2(7/14) – 7/14 log2(7/14) = 1/2 + 1/2 = 1
[High impurity, low homogeneity -> no good]

Note: 0 <= p <= 1, 0 <= entropy <= 1

All +1 or All -1 -> 0 entropy, “no information” . Max for S with 1/2 + and 1/2 - examples

Selecting the best attribute: information gain definition
• Information gain is the expected reduction in entropy caused by partitioning the examples on an attribute.
• Expected reduction in entropy knowing A 

Def. Gain:
	[Img. 13-3]

• The higher the information gain the more effective the attribute in classifying training data 
(higher variation in the homogeneity of the class distribution over the sub sets, 
max separation of classes).
• Homogeneous, as [14+, 0–] or [0+,7-] allow us “clear” classification

Selecting the best attribute: information gain: why?
• Entropy to measure the homogeneity (indeed impurity) of the class of the subset of examples, hence:
• Select A that maximize Gain
	After splitting, lower values (more homogeneous targets) in each subsets -> higher Gain 
• The aim is to separate the examples on the basis of the target, finding the attribute 
that discriminates examples that belong to different target classes
	– e.g. all the – on the left, all the + on the right

Select the best attribute: example
	[Img. 13-4]

Going on 
– The information gain is computed for the all the attributes and the one with highest inf. gain 
is selected as the first decision node (e.g. outlook)
– The training data are partioned for values of outlook (and associated to following nodes)
– If entropy is not zero in a set, the tree continues to grow there 
(with such data and remaining attributes).
– Obtaining the flowing DT

Problems with information gain
• The information gain favors attributes with many possible values.
• Consider the attribute Date in the PlayTennis example.
	– Date has the maximum information gain: Every day correspond to a different subset which is pure 
		-> 0 entropy
	– Perfect fit (separation) of TR data
	– But it is not significant: not useful for unseen instances!
• How to avoid generation of many small subsets?

An alternative measure: gain ratio

GainRatio(S, A) = Gain(S, A) / SplitInformation(S,A)
where SplitInformation(S,A) = [Img. 13-5]
• SplitInformation measures the entropy of S with respect to the values of A. 
The more uniformly dispersed the data the higher it is.

• GainRatio penalizes attributes that split examples in many small classes such as Date. 
Let |S| = n, Date splits examples in n subsets.
	SplitInformation(S, Date) = −[(1/n) log2(1/n))+ ... + (1/n) log2(1/n)] = −log2(1/n) = log2(n)
	which is > 1 for n > 2 -> we reduce the GainRatio
• Compare with an A which splits data in two even classes (with (n/2)/n= 1/2):
	SplitInformation(S, A)= − [(1/2) log2(1/2) + (1/2) log2(1/2)]= −[−(1/2) −(1/2)] = 1

Adjusting gain ratio
• Problem: SplitInformation(S, A) can be zero or very small when |Si| ≈ |S| for some value i [log 1 = 0]
	– E.g. An extreme case with |S1| = 0, |S2| = n
	– SplitInformation = - [0/n * log 0/n + n/n * log n/n] = - 0 - 0 = 0
	– E.g. an attribute with the same value for the examples, not good indeed!
• To mitigate this effect, the following heuristics has been used:
	1. compute Gain for each attribute
	2. apply GainRatio only to attributes with Gain above average
• Other measures have been proposed...

Hp Space Search in DT learning

Hp space search by ID3, Search (hill-climbing) through the space of possible DT 
from simplest to increasingly complex

WRT to previous alg. (Cand. Elimin.):
▪ The hypotheses space is complete (represents all discrete-valued functions)
▪ The search maintains a single current hypothesis
▪ No backtracking; no guarantee of optimality (local optima)
▪ It uses all the available examples (not incremental)
▪ May terminate earlier, accepting noisy classes

Inductive bias in DT learning
▪ What is the inductive bias of DT learning?
	1. Shorter trees are preferred over longer trees
		-> Due to simple-to-complex search.
		Not enough. This is the bias exhibited by a simple breadth first algorithm 
		generating all DT's and selecting the shorter consistent one
	2. Prefer trees that place high information gain attributes close to the root

▪ Note: DT's are not limited in representing all possible functions.
▪ The restriction is not over the Hp space, it is on the search strategy.

Two kinds of Biases
▪ Preference or search biases (due to the search strategy)
	- ID3 searches a complete hypotheses space; the search strategy is incomplete
▪ Restriction or language biases (due to the set of hypotheses expressible or considered)
	- Candidate-Elimination searches an incomplete hypotheses space; 
	the search strategy is complete (all the consistent hp)
▪ A combination of biases in learning a linear models.

Why the search bias can be preferred over the language bias?
▪ In ML typically use flexible approaches (universal capability of the models), 
without excluding a priori the unknown target function
▪ Of course, flexible -> overfitting issue!

Prefer shorter hypotheses: Occam's razor
▪ Why prefer shorter hypotheses?
	- Again, The Occam (Ockham) razor
	“The simplest explanation is more likely the correct one” 
	Or “prefer the simplest hypothesis that fits the data”
	- Lex parsimoniae ("law of parsimony", "law of economy", or "law of succinctness")
▪ The term razor refers to the act of shaving away unnecessary assumptions 
to get to the simplest explanation.
• Remember the “control of model complexity” by regularization for linear models
• This fundamental concept in ML will be found again and we will “rationalize” it at the end

Issues in decision trees learning
▪ Overfitting
	- Reduced error pruning
	- Rule post-pruning
▪ Extensions (specific for DT):
	- Alternative measures for selecting attributes [done]
	- Continuous valued attributes
	- Handling training examples with missing attribute values
	- Handling attributes with different costs
	- Improving computational efficiency

Overfitting: definition
• Building trees that “adapt too much” to the training examples may lead to “overfitting”.
• Consider error of hypothesis h over:
	– training data: errorD(h)			empirical error
	– entire distribution X of data: errorX(h)	expected or true error

• Hypothesis h overfits training data if there is an alternative hypothesis h' appartenente ad H such that:
errorD(h) < errorD(h’) and 
errorX(h’) < errorX(h)
i.e. h’ behaves worse on TR data, better over unseen data

Flexible approaches can easily encounter overfitting.

“Avoiding”* overfitting in DT
[“Avoiding” is not correct, we can see the methods to mitigate the overfitting, 
but we have still to control it by a conscious management]
Two strategies:
1. Stop growing the tree earlier, before perfect classification
2. Allow the tree to overfit the data, and then post-prune the tree

How to assess the effect?
▪ Training and validation set
	- split the training set in two parts (training and validation) 
	and use validation set to assess the utility of post-pruning
▪ Other approaches:
	- Use a statistical test to estimate effect of expanding or pruning
	- Minimum description length principle: uses a measure of complexity of encoding the DT 
	and the examples, and halt growing the tree when this encoding size is minimal

Reduced-error pruning
▪ Each node is a candidate for pruning
▪ Pruning consists in removing a subtree rooted in a node: the node becomes a leaf 
and is assigned the most common classification
▪ Nodes are removed only if the resulting tree performs no worse on the validation set.
▪ Nodes are pruned iteratively: at each iteration the node whose removal most increases accuracy 
on the validation set is pruned.
▪ Pruning stops when no pruning increases accuracy

Rule post-pruning
1. Create the decision tree from the training set
2. Convert the tree into an equivalent set of rules
	– Each path corresponds to a rule
	– Each node along a path corresponds to a pre-condition
	– Each leaf classification to the post-condition
	e.g. (Outlook=Sunny) && (Humidity=High) -> (PlayTennis=No)
3. Prune (generalize) each rule by removing those preconditions whose removal improves accuracy...
	– ...over validation set
	– ...over training with a pessimistic, statistically inspired, measure (heuristic)
4. Sort the rules in estimated order of accuracy, and consider them in sequence 
when classifying new instances

Why converting to rules? 
▪ Each distinct path produces a different rule: a condition removal 
may be based on a local (contextual) criterion.
▪ Pruning of preconditions is rule specific, node pruning is global and affects all the rules
▪ Converting to rules improves readability for humans

Dealing with continuous-valued attributes
▪ So far discrete values for attributes and for outcome.
▪ Given a continuous-valued attribute A, dynamically create a new attribute Ac
	Ac = True if A < c, False otherwise
▪ How to determine threshold value c?

Example. Temperature in the PlayTennis example
- Sort the examples according to Temperature
- Determine candidate thresholds by averaging consecutive values where there is a change in classification
- Evaluate candidate thresholds (attributes) according to information gain. 
The new attribute competes with the other ones

Handling incomplete training data (imputation)
▪ How to cope with the problem that the value of some attribute may be missing?
	- Example: Blood-Test-Result in a medical diagnosis problem
▪ The strategy: use other examples to guess attribute (within training data at a given node)
	1. Most common. Assign the value that is most common 
	among all the training examples at the node/those in the same class
	2. Assign a probability to each value, based on frequencies, and assign values to missing attribute,
	according to this probability distribution (adding more examples weighted by prob.)
▪ Missing values in new instances to be classified are treated accordingly (weighting), 
and the most probable classification is chosen

Handling attributes with different costs
• Instance attributes may have an associated cost:
we would prefer decision trees that use low-cost attributes
• ID3 can be modified to take into account costs:
1. Tan and Schlimmer
	Gain^2(S, A)/Cost(S, A)
2. Nunez
2^(Gain(S, A)) − 1/(Cost(A) + 1)^w	w appartenente a [0,1]

A geometrical view 
• Decision boundaries that can be produced by a DT:
Decision Trees divide the input space into axis-parallel rectangles 
and label each rectangle with one of the K classes (leaf of the tree)
	[Img. 13-6]

Conclusions
• DT is a popular approach for classification in a discrete number of classes.
	– Expressive hypotheses space in the area of propositional - rule based approaches.
	– Robust to noisy data. Deal with Missing attribute values.
	– Easy to be understood (explicit if-then rules, unless they are an huge amount)
	– Many extensions to the basic scheme...
• Language and search biases: ID3 searches a complete hypothesis space, with a greedy incomplete strategy
• Flexible approach: Overfitting is an important issue, 
tackled by post-pruning and generalization of induced rules

Introduction to Validation and Theoretical Issues

Obiettivi (overview) 
Questioni fondamentali del ML:
evaluate generalization capabilities (of your hp)
	– ruolo essenziale della validazione
	– cenni (dell’esistenza) di fondamenti teorici (supporto al significato del ML)

• Aspetto sia teorico che pratico per un uso consapevole del ML

ML issues
Quando un modello di ML è un buon modello?
Usare il ML versus usare bene il ML

Machine Learning: generalization
• Learning: search for a good function in a function space from known data
• Good w.r.t. generalization error: it measures how accurately the model predicts 
over novel samples of data (low error, high accuracy and vice versa) 

• Inductive learning hypothesis
	– Any h that approximates f well on training examples 
	will also approximate f well on new (unseen) instances x (?)
• Punto centrale, ma come obiettivo del ML:
	– Teoria che supporta in che condizioni ciò si verifca
	– Guida la scelta del “best model” 
	(tra modelli diversi o configurazioni diverse: iperparametri, livello di training...)
	– Va verificato nelle applicazioni

• Generalization: crucial point of ML!
• Learning phase (training, fitting): build the model from know data – training data (and bias)
• Predictive phase (test): apply to new example
	- we take the input x and we compute the response by the model; 
	we compare with its target that the model has never seen: 
	evaluation of the predictive hypothesis, i.e. of the generalization capability

Note: performance in ML = predictive accuracy 
estimated by the error computed on the (Hold out) Test Set
• Overfitting: A learner overfits the data if it outputs a hypothesis h(.) in H having true error eps
and empirical (TR) error E, but there is another h’(.) in H having E’ > E and eps’ < eps

Premise: which measure?
Recap:
To evaluate typically we measure...
• For classification: MSE for the loss, accuracy or mean error rate for the outcome
	– but also precision, recall or specificity, sensitivity 
	(accounting for False Positive, False Negative)...
• For regression: MSE, Root MSE (S), Mean Absolute Error, Max Absolute Error...
	– but also statistics measures such R (correlation coefficient/index ), etc.
• Of course high error <-> low accuracy (both for training, test, etc.)
	– E.g. poor fitting with high training error...
	– E.g. poor generalization with high test error...

Validation: Two aims
• Model selection: estimating the performance (generalization error) of different learning models 
in order to choose the best one (to generalize).
	– this includes searching for the best hyper-parameters of your model
	(e.g. polynomial order, lambda of ridge regression...)
	- It returns a model
• Model assessment: having chosen a final model, estimating/evaluating its prediction error/risk
(generalization error) on new test data (measure of the quality/performance of the ultimately chosen model).
	- It return an estimation

Hold out
• If data set size is sufficient: e.g. 50% TR, 25% VL, 25% TS disjoint sets

• TR: Training set is used to fit 							[training]
• VL: Validation set (or selection set) can be used to select the best models
(e.g. hyper-parameters tuning) 								[model selection]
• TR+VL sometimes are jointly called development/design set, i.e. used to build the final model
• TS: Test set is used for estimation of generalization error (of the final model) 	[model assessment]

Notes:
1) the estimation made for model selection (on VL set) is for model selection purpose, 
it is not a good estimation for the assessment phase/risk test.
2) Test set cannot be used for model selection (or call it validation set)

Test or model selection?
• What if test set is used in a (repeated) design cycle?
	– We are making model selection and not reliable assessment 
	(estimation of expected generalization error)
		-> and we wouldn't be able to do that on future examples
		-> Blind test set concept (e.g. for ML competitions)
		-> Image an exam exercise: if you see the solutions it is not a test!
	– In that case, used test set error provides an overoptimistic evaluation of the true test error 
	(we will see how easy is to obtain very high classification accuracy over random task 
	even using the test set only implicitly)

Gold rule: Keep separation between goals and use separate sets
(TR for training, VL for model selection, TS for risk estimation)
TR = training set, VL = validation set, TS = test set

TR/VL/TS by a simple schema:
	[Img. 14-2]

A simple meta-algorithm
• Separate TR (training), VL (validation) and TS (test) sets
• Search best h_w,λ() changing the model hyper-parameters λ 
[e.g. the polynomial order, the lambda for ridge regression]:
For each different values of λ (grid search):
	– Search best h_w,λ() that minimizes error/empirical loss (fitting the TR set) 
	finding the best w parameters, where best = minimum error on TR set [argminw Loss(w) in L2]
• Select the best best h_w,λ(): where best = minimum error on the VL set
• (Optional: Now it is also possible to fit h_w,λ(x) on TR+VL with best λ model)
• Evaluate the final h_w,λ(x) on the TS

Search on a grid (e.g. with 2 hyper-parameters)
• Find hyper-parameters value (i.e. parameters that are not directly learnt, 
which are not modified by training)
• Search best hyper-parameter can be a <<FOR>> over a grid of candidate values. 
For each trained model h_w,λ compute the results (accuracy) on the VL set. 
Then take the one with the minimum error or the max accuracy.

Controesempio (separare VL and TS)
	– 20-30 esempi, 1000 variabili di input random,
	– random target 0/1
	– Scelgo 1 modello con una sola variabile/feature che indovina 'per caso' 
	al 99% su qualsiasi split successivo in training, validation e test set.
Perfect result (a model with accuracy 99% )? What is wrong?
99% non è una buona stima dell’ errore di test (quella corretta e' 50%)

1. Errore stimato su training o validation per model selection NON è utile per stima del rischio!
2. Usare tutto il data set per feature/model selection lede la correttezza della stima
(risultati biased – «Feature Selection bias»).
	– Test set è stato usato implicitamente all’inizio).
	– Test deve essere separato prima, prima di qualsiasi model selction (incluso selezione di features)
Un test set esterno fornisce invece la stima corretta del 50% (random coin result!).
È la correttezza della stima che è in giudizio, non la possibilità di risolvere il task!

Delicato confrontando metodi diversi e usando tecniche di K-fold cross-validation 
che in sé non garantiscono correttezza della procedura di validazione.

Hold out and K-fold cross validation
Hold out CV can make insufficient use of data

K-fold Cross-Validation
• Split the data set D into k mutually exclusive subsets D1, D2, ..., DK
• Train the learning algorithm on D\Di and test it on Di
• Summarize averaging all the Di results
• It uses all the data for training and validation or testing
• NOTE: This technique can be used both for the validation set or for the test set

Issues:
• How many folds? 3-fold, 5-fold, 10-fold, ..., 1-leave-out
• Often computationally very expensive
• Combinable with validation set, double-K-fold CV...

An example of model selection and assessment (with K-fold CV)
• Split data in TR and Test set (here simple hold-out or a K-fold CV)
• [Model selection] Use K-fold CV (internal) over TR set, obtaining new TR e VL set in each folder, 
to find best hyper-parameters of your model (e.g. polynomial order, lambda of ridge regression...):
apply a grid-search with many possible values of the hyper-par.
	– i.e. for example a k-fold-CV for λ = 0.1, a k-fold-CV CV for λ = 0.01...
	and then take the best λ (comparing the mean errors computed over the validation sets 
	obtained by the all the folds of each k-fold CV)
• Train on the whole TR set the final model
• [Model assessment] Evaluate it on the external Test set

Validation: summarizing
• Stima Empirica: errore calcolato/stimato su (Hold out)
	– E.g. Hold out: training, validation set and test sets
	– K-fold cross validation (resampling)
• Teoria: E.g. Statistical Learning Theory
	– sotto quali condizioni (matematiche) un modello è capace di generalizzare (buona generalizazione)?

Typical behavior of learning
- Training and test errors are high: UNDERFITTING
	-> the model is too simple w.r.t. to the target function both for known data and new data
- Training error is low, test error is high: OVERFITTING
	-> the model is too complex: Fit the noise.

Toward SLT
Putting all together:
• The generalization capability (measured as a risk or test error) of a model
	– with respect to the training error
	– overfitting and underfitting zones
• The role of model complexity
• The role of the number of data

• Statistical Learning Theory (SLT): a general theory relating such topics

Formal Setting Statistical Learning Theory (SLT):
	[Img. 14-3]

Vapnik-Chervonenkis-dim and SLT: a general theory
• Given the VC-dim (VC), a measure complexity of H (flexibility to fit data) 
(e.g. Num. of parameters for linear models/polynomials)
	- Can we use Remp to approximate R?

• VC-bounds: [Img. 14-4]

• First (basic) explanation:
– ε is a function directly proportional to VC (VC-dim), inversely proportional to l and delta.
– We know that Remp decreases using complex models (with high VC-dim)
– delta is the confidence, it rules the probability that the bound holds 
(e.g. low delta 0.01, it holds with probability 0.99)
• Now we can see how it can “explain” the underfitting and overfitting and the aspects that control them. 

Intuition:
• Higher l (data) -> lower VC confidence and bound close to R
• Too simple model (low VC-dim) can be not suff. due to high Remp (underfitting)
• Higher VC-dim (fix l) -> lower Remp but VC-conf. and hence R may increase (overfitting)

• Concept of control of the model complexity (flexibility):
trade-off between model complexity and TR accuracy (fitting)

Discussion Complexity control
• Statistical Learning Theory (SLT):
	– Permette inquadramento formale del problema della generalizzazione e underfitting/overfitting, 		fornendono limitazioni superiori analitiche e quantitative al rischio R di predizione 
	su tutti i dati,  indipendemente dal tipo di learning algorithm o dettagli del modello.
	– Il ML è ben fondato:
		• Il rischio del learning (e l’errore di generalizzazione) 
		può essere analiticamente limitato, e solo pochi concetti sono fondamentali!
		• Si può trovare un buona approssimazione del f target da esempi, 
		pur di avere un buon numero di dati e una adeguata complessità del modello 
		(misurabile formalmente con la VC-dim)
	– Porta a nuovi modelli (SVM) (e altri metodi che direttamente considerino 
	il controllo della complessità nella costruzione del modello)
	– Fonda uno dei principi induttivi sul controllo della complessità

Domande aperte:
• Quali (altri) principi vi sono per fondare il controllo della complessità e come operare in pratica?
	– Come misurare la complessità (flessibilità per il fitting)?
	– Come trovare il bilanciamento ottimo tra fitting e complessità?

Some Examples for Complexity Control
• Linear models (LM):
	– (seems related to) number of free parameters w: input dimension/dim. of the basis expansion 
	(e.g. polynomial degree)
	– Lambda parameter for the regularized version
• Decision trees (DT): number of nodes
• We will see: direct approach to the complexity optimization through the SVM model

Conclusioni
• ML models flexiblity
	– Using the power of ML without control is a way to produce illusory results
	– Control the tradeoff between model fitting and complexity
	– Fundamental role of validation approaches (for model selection and estimations)
• Il ML è ben fondato teoricamente
	– Domande fondamentali tramite Statistical Learning Theory
	– ed altre (e.g. PAC-probably approximately correct learning)

Introduction to the use of SVM

Support Vector Machine (SVM) intro
• A classifier derived from statistical learning theory
• After years of theoretical developments, SVM became famous when, using images as input, 
it gave accuracy comparable to SotA neural-network (in the 90s) with hand-designed features 
in a handwriting recognition task
• Currently, SVM is widely used all the application fields of supervised learning
	– Also used for regression (will not cover)

SVM?
• you may be tempted to use it (e.g. popular sw tools)
• After all, it is close to our view of linear models...
• And an opportunity to see at least 1 model at the state-of-the-art

Indeed we restart from linear model for classification.
We are interested in enrich it for non-linear problems.

Our Aims for SVM intro
Objectives of this SVM intro in IIA are to show:
1) Control of the model complexity via optimization approach
	– to directly approximate the Structural risk minimization
	-> [Max margin classifier]
2) Use efficiently linear basis expansion via kernel
	– so we obtain another flexible approach for non-linear supervised learning
	-> [Kernel]
3) Avoid typical misinterpretations in the use of SVM
– Such are overoptimistic beliefs on overfitting and curse-of-dimensionatilty avoidance
	-> [Practice]

Classification by linear decision boundary
The classification may be viewed as the allocation of the input space in decision regions (e.g. 0/1)
Example: linear separator on 2-dim instance space x = (x1, x2) in R^2, f(x) = 0/1 (or -1/+1)

(x) = {1 if wx + w0 >= 0	[0, 1] outputs
       0 otherwise}
h(x) = sign(wx + w0)		[-1, +1] outputs
	-> Linear threshold unit (LTU)

AIM 1
1) Maximum margin classifier
• Binary classification problem
• Let us start assuming a linear separable problem
• and assuming also no noise data (hard margin SVM)

(we will release later these assumptions)

Margin examples
• Not all the hyperplanes solving the task are equals...
• Varying the separating hyperplane the margin varies as well.

The margin is (the double of) the distance between the hyperplane and the closest data points.
Toward max margin classifier...
	-> Intuitively: max distance to the data points, max “safe zone”

Toward max margin optimization problem
Consider the problem to learn a linear model for binary classification, 
i.e. a function h: R^n -> {-1,1} based on examples (xp, yp)

Training problem: find (w, b) such that all points are classified correctly and the margin is maximized

Canonical representation of the hyperplane [Img. 15-1]: 
	(xp, yp) is classified correctly for all p
	<-> w^Txp + b >= 0 if yp = 1 and w^Txp + b < 0 if yp = -1 for all p
w.l.o.g. (it is possible to rescale w, b so that the closest points to the separating hyperplane
satisfy |wT xp + b| = 1, i.e the support vectors):
	w^Txp + b >= 1 if yp = 1 and w^Txp + b <= -1 if yp = -1 for all p
	<-> (w^Txp + b) yp >= 1 for all p <- constraints: all points are correctly classified

Two Useful Facts
• Margin = 2/|w| [|w|^2 = (w^Tw)]
	maximize margin <-> minimize |w| <-> minimize (|w|^2)/2
• VC-dim of the SVM is inverse to the margin -> control of model complexity by the margin
The optimal hyperplane is the hyperplane which maximizes the margin (and solves the training problem)

Hard margin SVM: Quadratic optimization problem
Training problem: find (w,b) such that all points are classified correctly and the margin is maximized
Training problem (primal form): 
	minimize (|w|^2)/2 (i.e. w^Tw) 			[Objective function]
	such that (wxp + b) yp ≥ 1 for all p = 1...l	[Constraints]

quadratic optimization problem (sw packages)

• Note: Direct minimization of model complexity (optimization function),
• holding solution (0 errors) in the constraints
• Note: Objective function is convex in w

Dual Problem
Dual formulation of training: Maximize_α Σ_iα_i – (Σ_ijα_iα_jy_iy_jx_i^txj)/2	i, j = 1...l
with α_i >= 0, Σ_iα_iy_i = 0

• Find optimal αp p=1..l (Lagrangian multipliers) by quadratic programming
• Convex -> unique solution
• Computational cost scales with l (num. of data) instead of n (input dimension)
• Dual formulation (computing alpha values) allows us to show: 
support vectors and a special form of the solution

Solution: the classifier h(x)
• With the alfa (computed in the dual form) we can compute (w, b)
	w = Σα_py_px_p p = 1...l 	b = y_k - w^Tx_k for any α_k > 0
Def. -> [Img. 15-2]
1) Alfa != 0 <-> support vectors (α_p != 0 -> x_p is a support vector)
	The solution is sparse and formulated only in terms of the SVs
	The hyperplane depends only from support vectors!
2) A special form of the solution: it is not even necessary to compute (w,b) explicitly 
to classify the points

Role of the inner product
• Data enter in form of dot products of pairs of points

Soft Margin
Hard margin for all the points may be too restrictive
Some errors can be allowed for noise tolerance and to provide larger margin
Solution: allow errors introducing slack-variables.

Slack variables ξ_i can be added to allow misclassification of difficult or noisy data points

Primal training problem: 
minimize (|w|^2)/2 + C∙Σ_pξ_p 
such that (wx_p+ b) yp ≥ 1 - ξp and ξp >= 0 for all p

positive ξ_p indicates an error or too small margin, C > 0 guides the number of allowed errors
(the indices of the ξ_p computed by the solver)

C: is a user defined hyperparameter!
Low C -> many TR errors are allowed -> possible underfitting
High C -> no TR errors are allowed -> small margin -> possible overfitting
But we lost the automatic approximation of SRM of hard margin!

AIM 2
Up to now only for linear separable problems... And for non-linear cases?

Kernel
2) Use efficiently linear basis expansion via kernel
	– so we obtain another flexible approach for non-linear supervised learning

Mapping to a High-Dimensional Space
• Map the data points in the input space to a high-dimensional (so called in SVM) feature space, 
where they can be linearly separable

linear separators here correspond to non-linear separators in original space

• Using LBE Φ(x) instead of x can be used
• However, we know that using high dimensional feature spaces (large basis function expansion) 
can be computationally unfeasible and more importantly can easily lead to overfitting 
without controlling the dimension of feature space and the complexity of the classier 
(complexity is here related to the input dimensionality, # of free parameters on the eq:)
	h_w(x) = sign(Σ_kw_kΦ_k(x))
• We are going to propose the Kernel approach to manage (implicitly) the feature space 
in the context of regularized modeling (where the complexity is margin dependent):
	- Thus, thanks to the automatized regularization of SVM, complexity of the classifier 
	can be kept small regardless of dimensionality in the new feature space.

Use Φ(x) instead of x
• In SVM it is not necessary to compute w and the data enter in form of dot products of pairs of points
and it is not even necessary to compute directly phi
• i.e. we can implicitly manage the feature space by a Kernel function
	[Img. 15-4]

Kernel
A kernel k: R^n x R^n -> R is a function such that some (possibly high dimensional) Hilbert space X 
and a function Φ: R^n → X exists with 
	k(xi, xj) = Φ(xi)^TΦ(xj)
i.e. a kernel is a potential shortcut to compute the dot product efficiently also in high dimensional spaces

We use the K function to compute directly the dot products in the feature space

Well-known popular Kernels
• Linear: K(xi, xj) = xi^Txj
	– Mapping Φ: x → 𝜙(x), where 𝜙(x) is x itself
• Polynomial of power p: K(xi, xj)= (1+ xi^Txj)^k
	– Mapping Φ: x → 𝜙(x), where 𝜙(x) has exponential dimension in k
• RBF (radial-basis function) Gaussian: [Img. 15-5]
	– Mapping Φ: x→ 𝜙(x), where 𝜙(x) is infinite-dimensional
	- RBF is a very popular choice: note it has a hyperparameter (sigma)
	- Very flexible, it can be used to make decision boundary around each points!
	- Low sigma -> narrow peaked Kernels -> patterns are similar only if very close
	and the classifier replies with the class of the closest point
	- Can be very powerful on TR discrimination but of course prone to overfitting

SVM completed
• We choose the trade-off parameter C, and the kernel function K (and its parameters)
• solve the optimization problem to find alfa
	– Computational cost scales with l (num. of data) instead of n (feature space dimension)
	– Modularity: change just the Kernel (with the same solver)
• The final model: 
	H(x) = sign(Σ_(p in SV) alfa_py_p K(xp, x))

AIM 3
- Practice

Avoid misinterpretation
• Avoid typical misinterpretation in the use of SVM
	– Such are overoptimistic beliefs on overfitting and course-of-dim avoidance
• Overfitting can occur without a careful selection of SVM hyperparameters: C, kernel, kernel parameters...
• Implicit treatment of High dim space is in the feature space not in the input space 
(assuming we project therein significant inputs)
• Validation techniques seen so far for model selection (e.g. C, kernel and kernel hyperparameters)
and model evaluation should be used rigorously as well

From LIBSVM guide (grid search suggestion):
- Transform data to the format of an SVM software
- Conduct simple scaling on the data
- Consider the RBF kernel K(x, y) = e^(-gamma||x-y||^2)			[gamma = 1/(2*sigma^2)]
- Use cross-validation to find the best parameter C and gamma
- Use the best parameter C and gamma to train the whole training set
- Test on a separate external set

Details
• Data preprocessing:
	– {red, green, blue} → (0, 0, 1), (0, 1, 0), (1, 0, 0) 		[1-of-k]
	– Linear scaling continuous values in range [-1, +1] or [0, 1]
	– [e.g. v-min/(max-min)]
• Model selection grid-search: e.g. C and gamma in RBF
	– With a table on the combinations of all the possible growing (exponential) values 
	to find good intervals, e.g.:
		C = 2^(-5), 2^(-3), ..., 2^15
		gamma = 2^(-15), 2^(-13), ..., 2^3
	- Then a finer grid-search can be performed

Conclusion
• SVM is very useful and popular advanced ML tool
	– Performance: often good, but not always the comparison is
favorable wrt other ML methods (NN and others).
• Coming from theory (SRM) is a good way to provide new ML approaches
• Combing the use efficiently linear basis expansion via kernel within a max margin approach 
allows to combine flexible models and the control of complexity
• Modularity of the kernel open new possibilities
• Avoid to think SVM outside of the validation needs!

K-NN, Unsupervised learning and other approaches

AIM
• This introductory course cannot cover all the aspects of the large area of Machine Learning
• We left a series of paradigms, models, and algorithms
• Let’s us have a look to some important (not seen so far) cases in the
	– Instance based approaches
	– Unsupervised learning tasks
	– Other...

An overview (for supervised learning)
• Discrete spaces:
	– e.g. Conjuction of literals, Decision trees (propositional rules)
	– Inductive grammars, Inductive Logic Programming...
• Continuous spaces:
	– E.g. Multiple Linear Regression, Linear threshold unit (LTU), polynomial regression, k-means...
	– SVM, Neural Networks
• Probabilistic/Generative
	– Traditional parametric models: density estimation (e.g. coin toss), discriminant analysis,
	polynomial regression...
	– Graphical models: Bayesian networks, Naïve Bayes, Markov models, Hidden Markov models...
• Instance-based
	– Nearest neighbor

K-NN: K-Nearest Neighbors (supervised learning)

1-Nearest Neighbor
• Simply store the training data <xp, yp> p= 1...l
• Given an input x (with dimension n)
• Find the nearest training example xi
	– Find i so that we have min d(x, xi) -> i(x) = arg min d(x, xp)
	- E.g. Euclidian distance
• Then output yi

1-nn
• Very flexible
• No misclassifications in TR data -> 0 training error 
	- what for test data?
• Decision boundaries is not linear: but it is quite irregular
• May be unnecessary noisy

K-Nearest Neighbors
• A natural way to classify a new point is to have a look at its neighbors, and take an average:
	avg(x) = 1/k Σ_(xi in Nk(x)yi
where Nk(x) is a neighborhood of x that contains exactly k neighbors (closest patterns according to d):
	– k-nearest neighborhood: K-nn.
• If there is a clear dominance of one of the classes in the neighborhood of an observation x, 
then it is likely that the observation itself would belong to that class, too. 
Thus the classification rule is the majority voting among the members of Nk(x). As before,
	h(x) = {1 if avg(x) > 0,5
		0 otherwise}
• For regression task: use directly the avg: mean over K-nn 

15-nn
The predicted class is chosen by majority vote amongst the 15-nearest neighbors.
• Still very flexible
• Some misclassifications in TR data
• Decision boundaries is not linear: it is still quite, although less, irregular
• Decision boundary adapts to the local densities of the classes

Complexity of K-NN
• Again... there is trade-off between underfitting and overfitting by the possible values of K
• Classic u-shape curve of the test error moving between a
	– extremely flexible case (K=1)
	– up to a very rigid model (K=l): 1 mean for all the data

K-nn: An extreme
• Not a global hypothesis for all the instances -> no model to be fit
	– We need to memorize all the input examples
	– Non parametric model (in contrast think to the parametric linear model 
	with a set of fixed size parameters w)
• Local estimations (by locally constant functions) vs global linear approximation/estimation 
of the target function (over the instance space)
• Lazy, memory based, instance-based, distance-based methods

Limits of K-nn: computational cost
• Note that K-nn makes the local approximation to the target function for each new example to be predicted:
The computational cost is deferred to the prediction phase!

Moreover: high retrieval cost
• Computationally intensive for each new input: 
computing the distances from the test sample to all stored vectors
	– The time is proportional to the number of stored patterns
	– “ad-hoc” proximity search algorithms to optimize
		–> E.g. by indexing the patterns
• Cost in space (all the data are stored)

Limitations: Curse of dimensionality
• When we have a lot of input variables (high n), 
K-nn methods often fail because of the curse of dimensionality
	– when the dimensionality d increases, the volume (side^d) of the space 
	increases so fast that the available data become sparse.
	– i.e. the amount of data needed to support the result 
	often grows exponentially with the dimensionality.
• Irrelevant features: The Curse of Noisy
	– if the target depends on only few of many features in x (e.g. 2 out 20), we could retrieve 
	a “similar pattern” with the similarity dominated by the large number of irrelevant features
	- It grows with the dimensionality

Distance based methods: a consideration and inductive bias
Distance or metric based approaches:
• Common line among e.g. K-means, K-NN and kernel-based approaches
• What is similar? Measure when couple of patterns are similar.
• Giving a metric (e.g. the Euclidian metric was assumed so far) 
poses a relevant bias on the solution (much more than the alg. details)
• The metric is typically domain dependent
	– E.g. two string in a language, in biology, etc.
	– Based on the prior knowledge of the domain expert
	– In some way, the same of feature engineering to represent the problem
• Looking forward: is it possible to learn the metric? Yes, NN, Learning Kernels...

K-means
Unsupervised learning

Tasks: Unsupervised Learning
• Unsupervised Learning: No teacher!
	- TR = set of unlabeled data <x>
• E.g. to find natural groupings in a set of data
	– Clustering (partition of data into clusters [subsets of similar data])
	– Dimensionality reduction/Visualization/Preprocessing
	– Modeling the data density	

Utility
In nature:
	– Example (Taxonomy): organize life forms: what are mammals?
	– Example (human learning): babies learn to recognize (“cluster”) familiar faces
	before they can understand human speech

In Data Analysis:
• Explorative data analysis
	– Discover data latent structure automatically
	– Find unknown patterns
• Preprocessing for other ML approaches
	– E.g. by dimensionality reduction
• Moreover: Unlabeled data is much cheaper to obtain
	– Examples: e.g. 10 million images (sampled frames from YouTube) 
	with state-of-the-art results on object recognition (22,000 categories)

Clustering
Partition of data into clusters/prototypes (subsets of “similar” data):
patterns within a valid cluster are more similar to each other 
than they are to a pattern belonging to a different cluster

H space for clustering 
• Goal: optimal partitioning of unknown distribution in x-space into regions (clusters) 
approximated by a cluster center or prototype.
• H: a set of vector quantizers x -> c(x) (that represent the cluster)
	- continuous space -> discrete space
• Example of Loss function: measures the vector quantizer optimality
• A common loss function would be the squared error distortion:
	L(h(xp)) = ||xp - c(xp)||^2

• The average value over the distribution of inputs 
is the average distortion or reconstruction or quantization error

K-means
• The k-means is the simplest and most commonly used algorithm employing a squared error criterion
• The k-means algorithm is popular because it is easy to implement, and it's in general efficient
• However, it has several drawbacks and limitations that we will see

Basic K-means Batch Alg.
LBG or generalized Lloyd algorithm
(1) Choose k cluster centers to coincide with k randomly chosen patterns 
or k randomly defined points inside the hypervolume containing the pattern set.
(2) Assign each pattern to the closest cluster center (the winner).
(3) Recompute the cluster centers (geometric centroid, i.e. mean) using the current cluster memberships.
(4) If a convergence criterion is not met, go to step 2. E.g.
	– no (or minimal) reassignment of patterns to new cluster centers,
	– minimal decrease in squared error.

Details
• Given the cluster centers c1...cK (vectors of dim n, as x)
• (2) For each x the winner is (the nearest prototype):
	i*(x) = arg min ||x - ci||^2
• Now x belong to cluster i*
• (3) For each cluster i the new mean (centroid) is:
	ci = \/|clusteri| * Σ_(j: xj in clusteri) xj

K-means limitations
• The number of clusters to find must be provided
	– Trials and-error to find the most suitable K
• Local minima of loss L(x) makes the method dependent on initialization
	– Run multiple times from different random initializations
	– Initialize with a heuristic
• It can work well for compact and hyperspherical clusters.
• No visualization properties
	– K-means does not allow us to project data in a lower dim space

Evaluation
• How is the output of a clustering algorithm evaluated?
• What characterizes a ‘good’ clustering result and a ‘poor’ one?
• Subjective: little in the way of ‘gold standards’
exists in clustering except in well-prescribed subdomains.
• Objective measures (no treated here): e.g. quantization error 
(but note that depends on the number of centroids)!
• But not “trivially” the label of a underlining classification task, 
called purity (entropy, mutual inf...) (else you can use a classifier)!
• Quality of model/clustering versus quality of results (domain dependent)

Other topics in Unsupervised
• Hierarchical Clustering -> dendrograms
• Principal Components, Curves and Surfaces
• Association Rules
• Independent Component Analysis and Exploratory Projection Pursuit
• Multidimensional Scaling
• ART (adaptive resonance theory) NN
• Self-organizing map (SOM) neural networks

Other approaches for preprocessing
Among the multitude of approaches it deserve to mention in this course:

• Dimensionality reduction (in unsup. Learning)
	– <x1,x2, ..., xn> -> <x'1, x'2, ..., x'n'> 	n > n’
	– where the new features can be a combination of the original ones.
	- E.g. PCA Principal Component Analysis
		–> New axis are computed along the directions of max variance 
		of the original manifold of data
• Feature selection
	– Where we choose a subset of all the features
	– Domain knowledge (features engineering)
	– Automatic features selection on the basis of their redundancy 
	or relevance in the task (the most informative)
	– Many approaches: The problem is difficult as the learning problem one.
• Outlier detection
	– Find unusual data values that are not consistent with most observations 
	(e.g. due to abnormal measurements errors)

Other tasks
• Reinforcement Learning (learning with right/wrong critic).
	– Adaptation in autonomous systems (especially in robotics)
	– “the algorithm learns a policy of how to act given an observation of the world. 
	Every action has some impact in the environment, and the environment provides feedback 
	that guides the learning algorithm”.
	– Instead of supervision for each step we have information about wins/losses 
	(rewards or punishment) for the final state
	– Actions need to maximize the amount of received rewards
	– The learning decide which actions were most responsible for wins/losses
• Semi-supervised learning
	– combines both labeled and unlabeled examples (typically in greater number) 
	to generate an appropriate function or classifier.
• Learn to rank: (e.g. for search engines)
	– When the input is a set of objects and the desired output is a ranking of those objects
• On-line learning: new examples are learned in time
• Structured domain learning and relational learning:
	– The input and/or output domain can be structured 
	in the form of sequences (signals, time series...)
	– Or even more complex: trees, graphs, networks.
		-> Vector patterns + relationships with other components
		-> Structured Input: Molecules, web pages as graph/network data...
		-> Structured Output: network data in social analysis, Parse tree from sentences...
• Neural Networks: for both supervised and unsupervised learning
	- Close to our view of Linear Threshold Unit (LTU):
	- Indeed, LTU is close to the basic unit of a Artificial NN, the perceptron.
	- A NN is a network of such non-linear units
		–> with universal approximation capability
	- Composing a very Flexible approach for any purpose of the ML.
		–> Gradient descent approach for learning (backprogation)

Neural Networks
Natural inspired models: Neural Networks
	– Studied as computing paradigms since the '40
	– Neurobiological inspiration
	– Nowadays: set of powerful computing models for function approximation 
	and with predictive capabilities supported by a rigorous theoretical ground (learning theory)

Why internal layers?
The internal (hidden) layer with non-linear units provides the NN with:
• The capability to extract by learning a new representation of data (learning abstract features)
• The new representations simplify the classification task at the last layer
• Non-linear in w adaptive basis expansion where the phi are learned (depend on w)! 
(but unfortunately it also leads to a non-linear optimization problem)
• Distributed representation (versus symbolic): similarity can be more easily 
treated by real values vectors
• Very flexible approach for non-linear tasks
• For both classification and regression tasks
• Universal approximation capability

Deep Learning (DL)
• E.g. by deep multilayer NN architectures
• Common aspects among different approaches:
	– Multiple layers of nonlinear processing units
	– Supervised or unsupervised learning of feature representations in each layer, 
	with the layers forming a hierarchy from low-level to high-level features/representations
	(different levels of abstraction).

Learning representations of data
• Representation learning versus the feature engineering approach (see Distance based methods)
• Automatically discover the representations (a.k.a. the features) needed for detection or classification
• Increase level of abstraction through different layers

Example: An observation (e.g., an image) can be represented in many ways such as a vector of intensity
values per pixel, or in a more abstract way as a set of edges, regions of particular shape, etc.
	- Edges form motifs, motifs assemble into parts (e.g. corner), 
	parts form specific objects (e.g. eyes)...

• Performs best when input information has some form of structure, 
e.g. spatial, temporal... (images, language, music...)

Combine to generalize
• And the abstract features can be “reused” at the higher levels.
• It can combine them to generalize to unseen (during training) cases:
	– Woman without glasses
	– Man with glass
		-> Woman with glass can be easily represented as well

DL advantages
• Exploit compositionality of internal representations:
	– An exponential gain in representational power, due to the fact that simpler concepts 
	represented in a layer of the network can be exploited as primitives many times by the next layer
	to represent more complex concepts, avoiding explicit combinatorial representation 
	(and learning) of features
	– E.g. you have to learn each word/sub-pattern but not directly all the possible combinations 
	(i.e. without having to see all the configurations), hence: 
	less examples are needed to reach good generalization capability!

DL results
• Deep network were difficult to be trained in the past, but combining:
	– improvement in the techniques for training of such huge models,
	– HPC (e.g. GPU) and
	– large data collections from industry and real applications (e.g. millions of images)
• they nowadays work very well making a revolution in the AI approach to real-world solutions
• “These methods have dramatically improved the state-of-the-art in speech recognition, 
visual object recognition, object detection and many other domains”

Find-S: 		language bias + search bias
Candidate-Elimination: 	language bias

Linear Models: 		language bias + search bias

ID3 (Decision Trees): 	search bias

SVM:

K-NN:			metric bias
K-Means:
```
