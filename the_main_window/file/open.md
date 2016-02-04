## File
### Open
File/Open用于打开保存在电脑上的声音文件，除了WAV格式外，还可以打开以下格式：

- Avisoft-DOS (*.DAT) ：以前基于DOS平台的Avisoft-SONAGRAPH使用的文件格式
- NeXT/SUN (\*.AU; *.SND) ：UNIX工作站使用的标准文件格式
- Apple AIFF (\*.AIF; *.SND) ：苹果公司产品使用的标准文件格式
- User-defined (\*.*) ：用户在“File/Import-Format...”中自定义的其它文件格式

另外，也可以通过将文件直接拖拽到主窗口的方式打开文件。

### Browse...
该对话框用于在多个声音文件中快速寻找某一个文件。所有在特定文件夹中的文件都会列出，包括它们的日期和文件名。“...”按钮可以用于选择其它文件夹的文件。“<”和“>”按钮用于打开上一个和下一个文件。“Play”用于回放选择的文件。当文件的数量很多时（超过200个），必须点击“Update”按钮以显示文件的创建和修改时间以及文件名。另外，列表中当前可见的我文件会被选中并显示这些内容。只有Avisoft-RECORDER 2.4b或更高的版本中才会显示文件创建日期。对于所有其它的文件，会显示最后修改日期。

如果“compress”选项是选中的状态，声音文件中的空白部分会被去除（详见“Remove silent sections”，英文版第80页）。“compress settings...”按钮会打开一个对话框，可以进行压缩的相关参数。

### File Open Setting...
该对话框包含一些声波文件在主窗口中如何被打开和显示的设置。这些设置决定了大声波文件的打开速度。

#### temp directory
该编辑框决定保存临时文件的目录，当该编辑框为空时，临时文件将存储在以下目录——<username>/文档/Avisoft Bioacoustics/Configurations/SASLab。

为临时文件设置只读存储盘（a RAM disk）可以显著提高大文件的处理速度。只读存储盘的大小必须超过所有的临时文件的大小。一般经验是，大小至少是原始声音文件大小的两倍。当设置只读存储盘时，建议禁用创建临时拷贝（do not create a temporary copy）,否则软件会自动复制一份每个声波文件到只读存储盘中。

#### do not create a temporary copy (limited undo!)
如果选中该项，所有的编辑操作将直接作用于原始声音文件。这将会加快大文件的打开速度，因为不再需要另外的文件复制过程。因此，处理大文件时请使用该选项，但是直接在原始文件上操作也可能具有一定的风险。

#### do not allow any editing
该选项会禁用所有的编辑功能。如果你不想对声音文件进行任何修改，可以勾选该选项。当“do not create a temporay copy”选项选中时，该选项会自动被勾选。
#### limit the initial view to the first xxx seconds
