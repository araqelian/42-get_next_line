# 🗣 Subject &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;get_next_line
<br><br>
<table>
  <tr>
    <td>Function name</td>
    <td>get_next_line</td>
  </tr>
  <tr>
    <td>Prototype</td>
    <td>char &nbsp;*get_next_line(int &nbsp;fd);</td>
  </tr>
  <tr>
    <td>Turn &nbsp;in &nbsp;files</td>
    <td>get_next_line.c,&nbsp; get_next_line_utils.c, &nbsp;get_next_line.h</td>
  </tr>
  <tr>
    <td>Parameters</td>
    <td>fd: &nbsp;The &nbsp;file&nbsp; descriptor&nbsp; to &nbsp;read &nbsp;from</td>
  </tr>
  <tr>
    <td>Return&nbsp; value</td>
    <td>Read &nbsp;line: &nbsp;correct&nbsp; behavior<br>NULL: &nbsp;there &nbsp;is &nbsp;nothing &nbsp;else &nbsp;to &nbsp;read, &nbsp;or &nbsp;an &nbsp;error &nbsp;occurred</td>
  </tr>
  <tr>
    <td>External &nbsp;functs.</td>
    <td>read, &nbsp;malloc, &nbsp;free</td>
  </tr>
  <tr>
    <td>Description</td>
    <td>Write &nbsp;a &nbsp;function &nbsp;that&nbsp; returns&nbsp; a &nbsp;line &nbsp;read &nbsp;from &nbsp;a &nbsp;file &nbsp;descriptor</td>
  </tr>
</table><br>

<ul>
<li>Repeated &nbsp;calls &nbsp;(e.g., &nbsp;using &nbsp;a &nbsp;loop) &nbsp;to &nbsp;your &nbsp;get_next_line() &nbsp;function &nbsp;should &nbsp;let&nbsp;
you &nbsp;read &nbsp;the &nbsp;text &nbsp;file &nbsp;pointed &nbsp;to &nbsp;by &nbsp;the &nbsp;file &nbsp;descriptor, &nbsp;one &nbsp;line&nbsp; at&nbsp; a &nbsp;time.<br><br>
<li>Your &nbsp;function &nbsp;should &nbsp;return &nbsp;the &nbsp;line &nbsp;that&nbsp; was &nbsp;read.&nbsp;
If &nbsp;there&nbsp; is &nbsp;nothing &nbsp;else&nbsp; to &nbsp;read&nbsp; or&nbsp; if&nbsp; an&nbsp; error &nbsp;occurred, &nbsp;it&nbsp; should &nbsp;return &nbsp;NULL.<br><br>
<li>Make &nbsp;sure&nbsp; that &nbsp;your &nbsp;function &nbsp;works&nbsp; as &nbsp;expected &nbsp;both &nbsp;when &nbsp;reading &nbsp;a &nbsp;file &nbsp;and &nbsp;when&nbsp;
reading &nbsp;from&nbsp; the&nbsp; standard&nbsp; input.<br><br>
<li>Please&nbsp; note &nbsp;that&nbsp; the &nbsp;returned &nbsp;line &nbsp;should &nbsp;include &nbsp;the &nbsp;terminating &nbsp;\n &nbsp;character,&nbsp;
except &nbsp;if &nbsp;the &nbsp;end &nbsp;of &nbsp;file &nbsp;was &nbsp;reached &nbsp;and &nbsp;does &nbsp;not &nbsp;end &nbsp;with &nbsp;a &nbsp;\n &nbsp;character.<br><br>
<li>Your &nbsp;header&nbsp; file &nbsp;get_next_line.h &nbsp;must&nbsp; at&nbsp; least&nbsp; contain &nbsp;the&nbsp; prototype&nbsp; of&nbsp; the&nbsp;
get_next_line() &nbsp;function.<br><br>
<li>Add &nbsp;all &nbsp;the&nbsp; helper &nbsp;functions &nbsp;you &nbsp;need &nbsp;in &nbsp;the &nbsp;get_next_line_utils.c &nbsp;file.<br><br>
<li>Because &nbsp;you &nbsp;will &nbsp;have &nbsp;to &nbsp;read &nbsp;files&nbsp; in &nbsp;get_next_line(),&nbsp; add &nbsp;this &nbsp;option&nbsp; to &nbsp;your&nbsp;
compiler&nbsp; call:&nbsp; -D&nbsp; BUFFER_SIZE=n&nbsp;
It&nbsp; will&nbsp; define &nbsp;the &nbsp;buffer&nbsp; size&nbsp; for &nbsp;read().&nbsp;
<br>The&nbsp; buffer&nbsp; size &nbsp;value &nbsp;will&nbsp; be&nbsp; modified&nbsp; by&nbsp; your&nbsp; peer-evaluators &nbsp;and &nbsp;the&nbsp; Moulinette&nbsp;
in &nbsp;order &nbsp;to&nbsp; test &nbsp;your &nbsp;code.<br><br>
<li>You&nbsp; will &nbsp;compile&nbsp; your &nbsp;code&nbsp; as&nbsp; follows &nbsp;(a&nbsp; buffer &nbsp;size&nbsp; of&nbsp; 42&nbsp; is &nbsp;used &nbsp;as &nbsp;an &nbsp;example):<br>
cc&nbsp; -Wall &nbsp;-Wextra &nbsp;-Werror &nbsp;-D &nbsp;BUFFER_SIZE=42 &nbsp;<files>.c<br><br>
<li>We &nbsp;consider &nbsp;that &nbsp;get_next_line()&nbsp; has &nbsp;an&nbsp; undefined&nbsp; behavior&nbsp; if &nbsp;the &nbsp;file &nbsp;pointed&nbsp; to&nbsp;
by&nbsp; the &nbsp;file &nbsp;descriptor &nbsp;changed &nbsp;since &nbsp;the &nbsp;last &nbsp;call &nbsp;whereas &nbsp;read() &nbsp;didn’t &nbsp;reach &nbsp;the&nbsp;
end&nbsp; of&nbsp; file.<br><br>
<li>We &nbsp;also &nbsp;consider&nbsp; that&nbsp; get_next_line()&nbsp; has&nbsp; an &nbsp;undefined &nbsp;behavior &nbsp;when &nbsp;reading&nbsp;
a&nbsp; binary &nbsp;file. &nbsp;However,&nbsp; you &nbsp;can &nbsp;implement &nbsp;a&nbsp; logical&nbsp; way &nbsp;to &nbsp;handle &nbsp;this &nbsp;behavior&nbsp; if&nbsp;
you &nbsp;want&nbsp; to.
</ul><br>
<b>Forbidden</b><br>
<ul>
<li>You&nbsp; are &nbsp;not&nbsp; allowed &nbsp;to&nbsp; use&nbsp; your&nbsp; <b>libft</b>&nbsp; in &nbsp;this &nbsp;project.
<li><b>lseek()</b> &nbsp;is&nbsp; forbidden.
<li>Global&nbsp; variables&nbsp; are &nbsp;forbidden.
</ul>
<br><br>

# ⭐️ Bonus &nbsp;part

<br>
<p>
This &nbsp;project &nbsp;is &nbsp;straightforward &nbsp;and &nbsp;doesn’t &nbsp;allow &nbsp;complex &nbsp;bonuses. &nbsp;However, &nbsp;we &nbsp;trust&nbsp;
your &nbsp;creativity. &nbsp;If &nbsp;you &nbsp;completed &nbsp;the &nbsp;mandatory &nbsp;part, &nbsp;give &nbsp;a &nbsp;try &nbsp;to &nbsp;this &nbsp;bonus &nbsp;part.
</p>
<br>
Here &nbsp;are &nbsp;the &nbsp;bonus &nbsp;part &nbsp;requirements:
<ul>
<li>Develop &nbsp;get_next_line()&nbsp; using &nbsp;only&nbsp; one &nbsp;static &nbsp;variable.
<li>Your &nbsp;get_next_line() &nbsp;can &nbsp;manage &nbsp;multiple &nbsp;file &nbsp;descriptors&nbsp; at&nbsp; the &nbsp;same &nbsp;time.
For &nbsp;example, &nbsp;if &nbsp;you &nbsp;can &nbsp;read &nbsp;from &nbsp;the &nbsp;file &nbsp;descriptors &nbsp;3, &nbsp;4 &nbsp;and &nbsp;5, &nbsp;you &nbsp;should &nbsp;be&nbsp;
able &nbsp;to &nbsp;read &nbsp;from&nbsp; a &nbsp;different &nbsp;fd &nbsp;per &nbsp;call &nbsp;without &nbsp;losing &nbsp;the &nbsp;reading &nbsp;thread &nbsp;of&nbsp; each&nbsp;
file &nbsp;descriptor &nbsp;or &nbsp;returning &nbsp;a &nbsp;line&nbsp; from &nbsp;another&nbsp; fd.&nbsp;
It &nbsp;means&nbsp; that&nbsp; you&nbsp; should&nbsp; be&nbsp; able&nbsp; to &nbsp;call &nbsp;get_next_line()&nbsp; to&nbsp; read &nbsp;from &nbsp;fd&nbsp; 3,&nbsp; then&nbsp;
fd &nbsp;4, &nbsp;then &nbsp;5, &nbsp;then&nbsp; once&nbsp; again&nbsp; 3, &nbsp;once &nbsp;again&nbsp; 4,&nbsp; and &nbsp;so &nbsp;forth.
</ul>
Append &nbsp;the&nbsp; <b>_bonus.[c\h]</b> &nbsp;suffix &nbsp;to &nbsp;the &nbsp;bonus &nbsp;part &nbsp;files.<br><br>
It &nbsp;means &nbsp;that, &nbsp;in &nbsp;addition &nbsp;to &nbsp;the &nbsp;mandatory&nbsp; part &nbsp;files, &nbsp;you &nbsp;will&nbsp; turn &nbsp;in &nbsp;the&nbsp; 3&nbsp; following&nbsp;
files:<br>
<ul>
<li>get_next_line_bonus.c
<li>get_next_line_bonus.h
<li>get_next_line_utils_bonus.c
</ul>

<br><br>

> [!NOTE]  
> Because of 42 School norm requirements:
> * Each function can't have more than 25 lines of code.
> * All variables are declared and aligned at the top of each function.
> * Project should be created just with allowed functions otherwise it's cheating.
