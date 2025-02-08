java c
CIT   596   -   HW2
This   homework   deals   with   the   following   topics
*      Computing   big-O   for   iterartive   algorithms
*   Designing   efficient   algorithms   with   loops
Student   Name:        
Collaborator(if   any)   :        (at   most   2   other   collaborators.)
•   Starting   from   this   HW   we   will   use   the   acronym   WEAPARTE.   This   stands   for   Write   an   Efficient   Algorithm   in   Plain   English/Pseudocode   (we   actually   prefer   simple   plain English   descriptions),   Analyze   its   Run   Time,   and   Explain   (briefly).
•   Note   that   real   code   being   submitted   as   an   algorithm   will   result   in   loss   of points.
•   For   a   question   that   involves   an   algorithm   that   we   cover   in   class,   you   can   use   the   final   big-O   result.      No   need   to   show   the   derivation   again.      For   example,   if   binary   search   shows   up   in   your   algorithm   you   can just   say    “we   know   binary   search   is   O(log   n).”    If   you   are   using   an   algorithm   that   was   done   in   class,   you   do   not   need   to   rewrite   the   pseudocode.
•   For   all   questions   in   this   HW   and   subsequent   HWs   the   goal   is   to   find   algorithms   that   are most efficient in   terms   of   big-O   analysis.    You   do   receive   partial   credit   if   your   algorithm   is   less   efficient   than   the   best.       You    do   not   receive   credit   though   if   your   algorithm   computes   an   incorrect   result.   So   be   sure   to   check   for   correctness   before   you   worry   about   efficiency.   In   most   cases   we   will   be   lenient   about   off by   one   errors.
•   HashMaps   are   not   allowed   unless   otherwise   specified.
•   Reminder:   Your   algorithm   should   not   rely   on   a   fancy   data   structure   in   a   particular   lan-   guage.   Remember that a software developer should   be   able   to   look   at   your   pseudocode   and   turn   it   into   real   code   in   C,   Java,   Python,   Scala,   any   “modern”   programming   lan-   guage.   So   no   HashSet,   TreeMap,   numpy   arrays   etc.
•   You   do   not   have   to   worry   about   tiny   edge   cases   like   empty   arrays,   empty   lists   etc.   Unless otherwise specified, it is safe to   assume that   an   array   contains   distinct   elements.
•   Unless   otherwise   specified,   you   should   write   your   algorithm   analysis   as   “In   the   worst   case,   this   algorithm   is   ....”   .
1.    (2   points)    Solve   this   recurrence   by   using   the   master   theorem.    Please   specify   what   a,   b,   and   c   are   before   using   the   theorem

2.    (5   points)    There    is    an    array    of   n    distinct   elements.       You    are    not    given    any    further   information   about   the   array.
Here   are   2   ways   that   are   proposed   in   order   to   find   the   minimum   element.   Analyze   the   run   time   of both   of them.    From   a   big-O   perspective   which   one   is   better?
•   Use   recursion,   attempt   1   (divide   and   conquer   style)

•   Use   recursion   in   a   different   manner   (leave   one   out   style)

3.    (5   points)    Given   the   following   nested   loop   snippet   of code,   what   is   the   run   time   of this   algorithm   in   big   O   terms.
for (i = n; i ≥ 1; i = i/3) do 
for (j = 1; j ≤ i/2; j = j + 1) do 
print("abc") 
Provide   a   Θ-bound   on   the   runtime   of the   code   snippet   in   terms   of   n.  代 写CIT 596 - HW2Java
代做程序编程语言  You   may   assume   n   is   a   power   of   3.
Please   provide   a   brief explanation.
You   might   find   the   formula   for   a   geometric   series   to   be   useful.

4.    (8   points)    I   have   an   array   called   SP   of   length   n    (assume   n   is   very   large.    Greater   than   million.)   which   contains   share   prices   for   GameStop.   Assume   the   array   contains   a   large   amount of data in chronological order.    SP[0] is the intial price, SP[1] is the next recorded   price   and   so   on.I   want   to   compute   the   best   profit   I   could   have   made   by   buying   a single share   at   a   certain   time   and   selling   at   a   later   time.       Obviously   you   have   to   buy   before   you   sell.   WEAPARTE   for this.Your   algorithm   should   return   the   value   for   the   best   profit   that   can   be   made   as   well   as   when   I   should   have   bought   and   when   I   should   have   sold.      For   the   buying   and   selling   times,   we just   need   the   array   indices.
For   example   if the   array   is   10,   5,   20 then your   max   profit   is   15   and your   indices   are   buy   at   index   1   and   sell   at   index   2.
You   can   assume   for   this   question   that   there   is   always   some   profit   that   can   be   made.
5.    (8   points)    You   and your friend   are given   $N by   the   CIS   department.    N   is some   positive   integer.You   are   told   to   go   to   an   art   gallery   and   buy   two distinct paintings   such   that   the   entire $N   gets   used   up.    For   the   purposes   of this   question   we   will   assume   that   there   is   no   tax   and   no   tip.   There   is   precisely   one   copy   of each   painting.   We   will   also   assume   that   each   painting   has   a   distinct   cost.
Take in   as input   an   array of all the   painting   prices   in   the   gallery   and   determine   whether   or   not   it   is   possible   to   spend   exactly   $N   by   buying   2   items.    That   is,   return   a   boolean.
Your   goal   should   be   to   do   this   in   an   efficient   manner   where   n   is   the   length   of the   array.   WEAPARTE   for this.
For   example   if the   gallery   has   the   following   painting   prices
[523, 129,   90, 1233, 210,   375]   and   you   had   $613   you   could   buy   the   very   first   painting   and   the   other   one   that   is   90   dollars.   So   you   would   return   true   in   this   case.
You   cannot   use   a   Hashmap/Hashset   for   this.
Hint   :   As   a   first   step,   sort   the   array   of prices.   You   can   use   the   fact   that   sorting   can   be   done   in   Θ(nlog   n)   via   mergesort.
6.    (4   points)    Count    the    total   number   of   array   element   comparisons(that   is,    comparing   array   element   i   with   array   element j)   involved   in   performing   the   following   sorts   on   the   array   [18, 8, -11, 2,   7, -1, 35,   5].    For all of these   algorithms   please   refer to   the   pseudocode   in the textbook   (Algorithms   Unlocked).
a)   selection   sort
b)   insertion   sort.
we    will   cover   insertion   sort   on    Tue.       This    question    will    barely    take    10    mins    once    you   understand   it.
We   do   not   need   an   explanation   for   this   question.      There   are   2   points   for   each   correct   answer.
Please   do   not   ask   us   to   solve   this   question for   you   in   office   hours







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
