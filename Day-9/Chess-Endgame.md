# Title: Chess End-Game 
-- King+Rook versus King+Pawn on a7 (usually abbreviated KRKPA7). The pawn on a7 means it is one square away from queening. It is the King+Rook's side (white) to move.

# Sources: 

(a) Database originally generated and described by Alen Shapiro. (b) Donor/Coder: Rob Holte (holte@uottawa.bitnet). The database was supplied to Holte by Peter Clark of the Turing Institute in Glasgow (pete@turing.ac.uk). (c) Date: 1 August 1989

# Past Usage:

Alen D. Shapiro (1983,1987), "Structured Induction in Expert Systems", Addison-Wesley. This book is based on Shapiro's Ph.D. thesis (1983) at the University of Edinburgh entitled "The Role of Structured Induction in Expert Systems".
Stephen Muggleton (1987), "Structuring Knowledge by Asking Questions", pp.218-229 in "Progress in Machine Learning", edited by I. Bratko and Nada Lavrac, Sigma Press, Wilmslow, England SK9 5BB.
Robert C. Holte, Liane Acker, and Bruce W. Porter (1989), "Concept Learning and the Problem of Small Disjuncts", Proceedings of IJCAI. Also available as technical report AI89-106, Computer Sciences Department, University of Texas at Austin, Austin, Texas 78712.
Relevant Information: The dataset format is described below. Note: the format of this database was modified on 2/26/90 to conform with the format of all the other databases in the UCI repository of machine learning databases.

Number of Instances: 3196 total

Number of Attributes: 36

Attribute Summaries: Classes (2): -- White-can-win ("won") and White-cannot-win ("nowin").

Class Distribution: In 1669 of the positions (52%), White can win. In 1527 of the positions (48%), White cannot win.
The format for instances in this database is a sequence of 37 attribute values. Each instance is a board-descriptions for this chess endgame. The first 36 attributes describe the board. The last (37th) attribute is the classification: "win" or "nowin". There are 0 missing values. A typical board-description is

f,f,f,f,f,f,f,f,f,f,f,f,l,f,n,f,f,t,f,f,f,f,f,f,f,t,f,f,f,f,f,f,f,t,t,n,won

The names of the features do not appear in the board-descriptions. Instead, each feature correponds to a particular position in the feature-value list. For example, the head of this list is the value for the feature "bkblk". The following is the list of features, in the order in which their values appear in the feature-value list:

[bkblk,bknwy,bkon8,bkona,bkspr,bkxbq,bkxcr,bkxwp,blxwp,bxqsq,cntxt,dsopp,dwipd, hdchk,katri,mulch,qxmsq,r2ar8,reskd,reskr,rimmx,rkxwp,rxmsq,simpl,skach,skewr, skrxp,spcop,stlmt,thrsk,wkcti,wkna8,wknck,wkovl,wkpos,wtoeg]

1	bkblk	the BK is not in the way

2	bknwy	the BK is not in the BR's way

3	bkon8	the BK is on rank 8 in a position to aid the BR

4	bkona	the BK is on file A in a position to aid the BR

5	bkspr	the BK can support the BR

6	bkxbq	the BK is not attacked in some way by the pro- moted WP

7	bkxcr	the BK can attack the critical square (b7)

8	bkxwp	the BK can attack the WP

9	blxwp	B attacks the WP (BR in direction x = -1 only)

10	bxqsq	one or more Black pieces control the queening square

11	cntxt	the WK is on an edge and not on a8

12	dsopp	the kings are in normal opposition

13	dwipd	the WK distance to intersect point is too great

14	hdchk	there is a good delay because there is a hidden check

15	katri	the BK controls the intersect point

16	mulch	B can renew the check to good advantage

17	qxmsq	the mating square is attacked in some way by the promoted WP

18	r2ar8	the BR does not have safe access to file A or rank 8

19	reskd	the WK can be reskewered via a delayed skewer

20	reskr	the BR alone can renew the skewer threat

21	rimmx	the BR can be captured safely

22	rkxwp	the BR bears on the WP (direction x = -1 only)

23	rxmsq	the BR attacks a mating square safely

24	simpl	a very simple pattern applies

25	skach	the WK can be skewered after one or more checks

26	skewr	there is a potential skewer as opposed to fork

27	skrxp	the BR can achieve a skewer or the BK attacks the WP

28	spcop	there is a special opposition pattern present

29	stlmt	the WK is in stalemate

30	thrsk	there is a skewer threat lurking

31	wkcti	the WK cannot control the intersect point

32	wkna8	the WK is on square a8

33	wknck	the WK is in check

34	wkovl	the WK is overloaded

35	wkpos	the WK is in a potential skewer position

36	wtoeg	the WK is one away from the relevant edge

In the file, there is one instance (board position) per line.
