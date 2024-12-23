java c
ENME4332   Finite   Element   Analysis   1
Fall   2024
Final   Project [100   points]
1          Project   DescriptionIn this project, we will solve a steady-state heat conduction problem within an   arbitrary   2D   domain   subjected   to   a   combination   of   prescribed   temperature   and   flux   boundary   conditions.    As   is   shown   in   Fig.      1,   this   2D   structure   consists   of two   parts   made   of different   materials   (material   1:   gray;   material   2:   pink)   with   different   conductance.   Please   note that the   heat   source   s   is   applied to the   inner   subdomains   highlighted   in   pink.    The   natural   boundaries   are   highlighted   in   red   and   blue   for   inward   and   outward   heat   fluxes,   respectively.      The   essential   boundaries   are   highlighted   in   green.Please   rigorously   follow the   dimensions   shown   in   Fig.    1.   With the   origin   of the   coordinate   system   located   at   the   left   bottom   corner,   the   center   coordinates   of the   two   circles   are   (0.4,0.7)   and   (1.6,0.7),   and   the   radius   is   0.1.   The   parameters   a   and   b   are   unique   values   assigned   to   each   student   in   a   separate   list.
The   strong   form   of the   governing   equations   for   this   problem   is   as   follows:

2          Abaqus   Modeling
Construct   the   2D   model   in   Abaqus   and   perform   the   following   tasks:
•    Mesh   the   domain   with   linear   triangular   elements.
•    Consider two mesh sizes.    The coarse mesh   has   around   250   -   300   elements,   and   the   fine   mesh   has   around   950-1000   elements.
•    Solve   the   problem   with   these   two   meshes   separately.
•    Save   the   mesh   details    (nodal   coordinates   and   element   connectivity)   for   both   mesh   sizes   into   separate   spreadsheets   or   text   files   for   the   subsequent   usage   in   our   own   matlab   code.
3            Matlab   Implementation
Write   a   MATLAB-based   FEM   program to   solve the   described   problem,   and this   set   of   code   has   three   major steps,   namely   pre-processing,   processing   and   post-processing.   In   the   pre-processing   step,   we   will:

Figure   1:   2D   domain   with   boundary   condition,   source,   and   dimensions.   Note   that   all   the   listed   dimensi代 写ENME4332 Finite Element Analysis 1 Fall 2024Matlab
代做程序编程语言ons   are   in   meters.
•    Define   the   material   properties.
•    Read the mesh generated by Abaqus to   construct the   nodal   coordinate   matrix   and   element   connectivity   matrix.
•    We   also   need   to   label   the   essential/natural   boundaries   and   flag   the   two   subdomains.   Then,   in   the   processing   step,   we   will:
•    Implement   the   element   conductance   matrix   Ke      (Eq.   8.10   in   the   textbook)   and   element   flux   matrix   fe   (Eq.   8.11)
•    Assemble   the   global   conductance   matrix   K   and   flux   matrix   f
•    Apply   essential   boundary   conditions   and   solve   for   the   unknown   temperature.
4          Post-processing   and   submissions
With   the   solutions   obtained   with   our   own   FEM   code,   perform   the   following   tasks.Note:    All   the   previously   listed   procedures   are   the   hints   that   guide   you   through   the   project.   The   following   questions   are where your   project will   get   accessed.    Please   organize your   submission   by   answering   each   of the   questions   clearly   with   correct   numbering.
1.    Plot   both   coarse   and   fine   mesh   you   generated   and   report   the   total   number   of elements.
2.    Create   2D   plots   of temperature   field   T(x,y)   with   both   coarse   mesh   and   fine   mesh   results.    Hint:    Use   the   ’patch’command   in   MATLAB.
3.   Plot   the   temperature   T(x,y    =   0.4)   along   the   line   y    =   0.4m   for   both   mesh   sizes   and   compare   with   Abaqus results.   Describe your observations.    Hint:    Use   x   coordinate   as horizontal   axis.    On each graph,   you   will   have   four   lines:   MATLAB   coarse,   MATLAB   fine,   Abaqus   coarse,   and   Abaqus   fine.
4.    Create   2D   patch   plots   of flux   magnitude    |q|(x,y)   and   2D   arrow   plots   of flux   at   center   of each   element   for   both   mesh   sizes.
5.    Plot   flux   magnitude    |q|(x,y    =   0.4)   along   the   line   y    =    0.4m   for   both   mesh   sizes   and   compare   with   Abaqus   results.   Describe   your   observations.
6.    Provide   a   better   mesh   strategy.
Due   date:    10-Dec-2024
Please   submit   a   zip   folder   containing   your   answers   in   PDF   and   MATLAB   code   to   Canvas.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
