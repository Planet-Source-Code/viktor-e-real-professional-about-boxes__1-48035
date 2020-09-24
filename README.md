<div align="center">

## REAL professional About boxes


</div>

### Description

A little use of inspiration for a magnificent effect...
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Viktor E](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/viktor-e.md)
**Level**          |Beginner
**User Rating**    |3.7 (11 globes from 3 users)
**Compatibility**  |VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/viktor-e-real-professional-about-boxes__1-48035/archive/master.zip)





### Source Code

Say, you got tired of the simple About boxes which you try time and again to improve by using text orientation effects and images but still can't get what you want - the ultimate About box ?.. Well, here's an idea how to obtain it with a little.. push.<br>
Ever heard of Macromedia Flash ? :) Of course you did ! Thought it is most useful on web pages presentations ? Wrong ! Why not use it outside them, say, in an About box ?? With just a little effort in learning Flash movie-making, you'll have the About box you ever wanted, and who knows - maybe more !<br>
Again, ever heard of custom resources ? Again, of course you did. Let's combine these two areas of.. computer science and get a LIVING About box.<br>
First of all, and most important, you do not have to distribute the movie separately from the program itself; that's why you'll use it as a resource. Steps to do it ? Here's some steps for you:<br>
1. Make the About movie (the hardest part of all, I agree... :) )<br>
2. Insert the .swf file as Custom resource, putting it in the category, say "AboutMovies", and giving it the ID "TheAboutMovie"<br>
3. Put a WebBrowser control on the form, dimensioning it to fit the size of the movie you made.<br>
4. Use it !<br><br>
Private Sub Form_Load()<br>
Dim moviebits() As Byte<br>
moviebits=LoadResData ("AboutMovies", "TheAboutMovie")<br>
Open App.Path & "\aboutmov.swf" For Binary Access Write As #1<br>
Put #1, , moviebits<br>
Close<br>
Erase moviebits<br>
WebBrowser1.Navigate2 App.Path & "\aboutmov.swf"<br>
End Sub<br><br>
Private Sub Form_Unload(..<br>
...<br>
Kill App.Path & "\aboutmov.swf"<br>
...<br>
End Sub<br><br>
End of HowTo.<br>
Try this at home. Regards.

