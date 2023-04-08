# How To Copy and Paste Text From ChatGPT

Ordinarily, when you try to copy and paste from ChatGPT, you often lose formatting or get weird backgrounds.

To avoid this, use the following approach:

1. Copy the text from ChatGPT as usual
2. Open LibreOffice Writer and paste there
3. Save as an .odt file
4. Use pandoc to convert the .odt to any format of your choice

I find it useful to convert to Markdown, as it is editable using basic text editors and preserves formatting and hyperlinks.

Note that this method is not unique to ChatGPT, and can be used with other websites as well.

To launch LibreOffice Writer easily, add the following command to your ~/.zshrc file:

```
alias writer='/Applications/LibreOffice.app/Contents/MacOS/soffice --writer'  #LibreOffice Writer
```

You can create an empty .odt file as follows:
`touch somefile.odt`

Then open it in LibreOffice Writer as follows:
`writer somefile.odt`

In LibreOffice Writer, paste in the content and save the .odt file.

Now convert it to markdown as follows:
`pandoc -o somefile.md somefile.odt`

You can now edit this markdown file in Visual Studio Code:
`code somefile.md`

Visual Studio Code has a nice plugin: Markdown Preview Enhanced, that allows you to preview changes to Markdown and copy/paste the output elsewhere, such as Gmail or another application. You can also easily paste this output to Substack or other publishing platform.

See these files for an example. This was created using ChatGPT's response to the question: `Can you suggest an itinerary for a 1 week trip to London with family?` and follow up question `Can you provide links for the places listed above?`

[somefile.md](somefile.md)
[somefile.odt](somefile.odt)