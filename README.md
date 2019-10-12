# OSU AI Club
[ description ]

## Usage
### Math Equation
[ description ]
```
$$
\begin{align}
[math_equation]
\end{align}
$$
```
```
$$
\begin{align}
v(t_1) &= v(t_0) + \int_{t_0}^{t_1} a(t) dt \\  
x(t_1) &= x(t_0) + \int_{t_0}^{t_1} v(t) dt \\
\end{align}
$$
```
### Tables
[ description ]
```
{% include built-in/table.html 
id="[table_id]" 
content="[table_content]" 
caption="[table_caption]" %}
```
```
{% include built-in/table.html 
id="0" 
content="

| First Header  | Second Header | Third Header         |
| ------------- | ------------- | -------------------- |
| First row     | Data          | Very long data entry |
| Second row    | **Cell**      | *Cell*               |
| Third row     | Cell that spans across two columns   ||

" 
caption="attadad" %}
```
### Pseudocode
[ description ]
```
{% include built-in/pcode.html id="1" code="
\begin{algorithm}
\caption{[algorithm_title]}
\begin{algorithmic}
[algorithm_code]
\end{algorithmic}
\end{algorithm}
" %}
```
```
{% include built-in/pcode.html id="1" code="
\begin{algorithm}
\caption{Quicksort}
\begin{algorithmic}
\PROCEDURE{Quicksort}{$A, p, r$}
    \IF{$p < r$} 
        \STATE $q = $ \CALL{Partition}{$A, p, r$}
        \STATE \CALL{Quicksort}{$A, p, q - 1$}
        \STATE \CALL{Quicksort}{$A, q + 1, r$}
    \ENDIF
\ENDPROCEDURE
\PROCEDURE{Partition}{$A, p, r$}
    \STATE $x = A[r]$
    \STATE $i = p - 1$
    \FOR{$j = p$ \TO $r - 1$}
        \IF{$A[j] < x$}
            \STATE $i = i + 1$
            \STATE exchange
            $A[i]$ with     $A[j]$
        \ENDIF
        \STATE exchange $A[i]$ with $A[r]$
    \ENDFOR
\ENDPROCEDURE
\end{algorithmic}
\end{algorithm}
" %}
```
### Single Image
[ description ]
```
{% include built-in/img.html 
id="[image_id]" 
url="[image_url]" 
caption="[image_caption]" %}
```
```
{% include built-in/img.html 
id="1" 
url="https://www.gwern.net/images/silkroad/2012-christin-sr-dailysales.png" 
caption="[image description]" %}
```
### Video
[ description ]
```
{% include built-in/vid.html 
url="[video_url]" %}
```
```
{% include built-in/vid.html 
url="https://www.youtube.com/embed/DM0nkQxrpW0" %}
```
### Code
[ description ]
````
```[language]
[code]
```
<output>[output]</output>
````
````
```python
# import relevant libraries
import roslib
import rospy
import math

def mb_callback(msg):
  # Check if robot has reached goal
  if msg.status.status == 2 or msg.status.status == 4 or msg.status.status == 5 or msg.status.status == 6:
    print "Robot failed to reach waypoint!"
  elif msg.status.status == 3:
    print "Robot successfully reached waypoint!"
  
  pub.publish(waypoint)
```
<output>Using TensorFlow backend.</output>
````
### Hint Box
[ description ]
```
{% include built-in/hint.html 
content="[text]" %}
```
```
{% include built-in/hint.html 
content="The program <code>nvidia-smi</code> allows you to monitor your GPU utilization and can help you understand bottlenecks in your data pipeline. The average GPU utilization should usually be above 70-80%." %}
```
### Quotes
[ description ]
```
> [quote]

```
```
> Ah! let not Censure term our fate our choice, / The stage but echoes back the public’s voice; The drama’s laws the drama’s patrons give, / For we that live to please must please to live.<br /> [Samuel Johnson](wikipedia.org/wiki/)(“Prologue at the Opening of Drury Lane Theatre”)

```
### Footnotes
[ description ]
```
{% include built-in/note.html
id="[id]"
details="[source]"
%}
```
```
{% include built-in/note.html
id="1"
details="https://www.youtube.com/watch?v=Q8nhQSp__3s&list=WL&index=11"
%}
```