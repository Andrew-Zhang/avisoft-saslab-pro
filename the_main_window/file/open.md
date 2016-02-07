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
当打开非常大的声波文件时，电脑会需要一段比较长的时间才能显示完整个波形，该选项可以通过只显示整个文件的开始部分以减少时间延迟。
#### covert frequency stereo to mono
如果勾选该选项，立体声道将自动转换为单声道，可以在“Settings...”中进行相关设置。
#### sampling frequency conversion
如果勾选该选项，会自动对声波文件重新取样，可以在“Setting...”中设置需要的取样率。
#### remove silent sections (breaks)
如果勾选该选项，会自动去处打开的文件中的空白间隔。通过比较振幅的阈值判断空白部分，可以在“Settings...”中设置阈值及其它参数。注意，该选项不能与“re-assemble consecutive files”同时选择。
#### change volume
该选项执行的操作是“Edit”/"Change volume..."，可以在“Settings...”中选择需要的操作。
#### Main window envelope display options
#### normalize envelope display
（详见英文版第51页）
#### fast envelope display mode (amplitude samples only)
如果勾选该选项，封波（如果将所有泛音在图上显现之振幅顶点连接，则会形成「频谱封波」(spectral envelope)，它对音色改变有很大的影响力。）显示将只基于一定数量的取样，因此，该选项可以加速大的声波文件的显示。然而，取样的降低可能会导致错误的显示，如果需要完整的和正确的封波显示，不要勾选该选项。
#### fast spectrogram display mode 
如果勾选该选项，声谱图的显示将只基于一定数量的取样，这可以加速大的声音文件的显示。样点之间的声音会被忽略，不会显示。
#### Optimize waveform and spectral envelope overviews
该选项会将波形和频谱封波保存在只读存储磁盘中以加速大文件在主窗口的显示。

**save envelopes to disk (\*.env)**：如果勾选该选项，经过内部运算的封波将保存到磁盘上（与wav文件相同的文件名，但扩展名是.env），这将加速之后的大文件的打开进度。.env文件也可以通过命令“Create envelope (.env) sidecar file”提前创建。

**envelope resolution (FFT frames)**：8-1024的设置决定内部存储的封波数据集的精度，数值越小创建的数据集越大、细节越丰富，而大的数值会减少数据集并且当中度缩放的时候预览会有更长的延迟。
#### Numbered event files creates by Avisoft-RECORDER
这些设置只对Avisoft-RECORDER软件录制的声音文件有效。
#### add neighbour channels
(详见英文版第37页)
#### display voice notes
该选项会显示与主声音文件相关的所有声音笔记。左键单击红色长方形按钮可以回放这些声音。声音笔记是普通的.wav格式的文件，文件名中包括主声音文件的名字，再加上“_noteXXX”的后缀以表明是声音笔记文件。
#### re-assemble consecutive files
可以使用“Setting”按钮设置该选项，详见英文版第34页。注意，该选项不能与“remove silent sections (breaks) ”结合使用。

“Fast!”按钮可以使“File Open command”中的设置尽快生效。
### Close
当前打开的文件会被关闭。
### Save
以当前的文件名保存当前文件。
### Save As...
以新的文件名保存当前打开的文件。如果文件中存在标记的部分，需要选择只保存标记的部分还是保存整个文件。除了标准的\*.WAV格式，还可以保存为\*.AU, \*.SND, \*.AIF或者ASCII格式。
### Rename
该命令用于重命名当前打开的文件。如下几个选项可以加快多个高质量文件的处理速度：

**keep original name string**：该选项可以保留当前文件名字符并插入新键入的字符作为前缀。当处理多个由Acisoft-RECORDER或其它第三方设备创建的声音文件时，建议使用该选项。

**Remove existing prefix**：该选项将去除已有的全部前缀并且使用一个新的代替。

**Hide this dialog box**：如果重命名命令是通过“Rename by text module”执行的，该选项会隐藏该对话框以减少键盘或鼠标操作。

**Automatically proceed to the next numbered file**：如果选中该选项，当重命名结束后，软件将自动打开下一个文件。

**Create LOG file entry**：该选项会创建一个日志文件或者将日志文件发送到Excel。使用“LOG file/DDE setting”按钮可定义日志文件名和格式一集可选的DDE(Dynamic Data Exchange，软件间共享数据的标准格式)输出。

新的文件名会显示在当前对话框的底部。重命名命令还会重命名所有相关的.kml或.gpx文件（具有相同文件名的文件）。
### Rename by text module/Define text module
重命名对话框还可以从菜单中的“Rename by text module/Define text module”执行，此时会粘贴预定义的文本模式（例如物种名等）。关联键盘快捷键（如F1...F12）可以进一步减少重命名操作。可以通过选择12个次级菜单，键入需要的字符，然后点击“Define as text module!”键来设置文本模式。必须取消“Rename by text module/Define text module”和“Hide dialog box”选项才能打开该对话框。已经定义好的文本模式还可以通过文本模式菜单按钮或者重命名对话框的组合框打开。

“Show text modules on touch panel”选项会在一个单独的、合适大小的触屏面板打开，以适用于在触屏设备上使用重命名功能。

当文本模式的数量超过12个时，可以通过次级菜单上的“File/Rename by text module/Define text module/External text file”功能继续添加。“Select external file...”命令可以打开一个存储有定义好的文本模式的文本文件，该文件中的文本模式之间需用CR/LF(<new line>)隔开。如果启用了“Use external file : xxxx”选项，此文本文件中的字符都会添加到“File/Rename”命令和“Insert label”命令的菜单中。

如果启用了“Paste text module into the first dXML field (instead of renaming)”选项，并且dXML对话框已打开，文本模式会被粘贴到第一个dXML区域中，重命名功能不会生效。
### Record
录音命令可以将声音采集进电脑，电脑必须安装声卡或者功能等同的带有多媒体拓展驱动的接口。

使用“File/Sound Card Settings...”命令选择取样频率、数字化位数和最大录制时间。取样频率应该适应要录制的信号。可以通过“File/Record”命令或点击录制按钮![Record button](record_button.png)开始录音。实时声谱图将显示在主窗口。录制可以通过点击停止按钮![Stop button](stop_button.png)随时取消。之后整个文件豆浆显示在主窗口中。如果声卡过载，封波的颜色会变成红色，此时应该降低录音层次并重试以防止录制信号的失真。
### Real Time Spectrogram
该菜单选项可以打开实时声谱窗口。（详见英文版210页）
### Sound card settings
该菜单选项用于调整声卡设置。可以选择采样频率、位数和最大录音时间。如果选中“Duration of Recording”，在设定的时间结束后录音会停止，否则录音只能手动停止（录音数据超过2GB也会停止）。

取样频率应该适应于要分析的信号，至少应该是要录制的信号的最大频率的两倍。如果声卡上有去锯齿过滤器，所有超过Nyquist频率（奈奎斯特频率，独立信号处理系统的采样率的一半）的信号都会被去除，若没有，超过Nyquist频率的信号会导致数字信号失真和错误的声谱图。现在，一般的声卡上都有模拟信号转数字信号的转换器，因此都会有烦锯齿过滤器。

注意，采样频率还会影响声谱图的频率精度，二者呈正比。

如果启用“Perform Sampling frequency conversion”选项，录音结束后，声卡根据设定的取样频率产生的原始文件会依据“Edit/Sampling Frequency Conversion”中的参数设置被重新取样。该选项允许快速生成声音文件，声卡本身不支持该功能。

当从实时声谱图窗口打开“Sound-card settings”对话框时，另外一个组合框“Down-sampling”也会打开。该选项可以进一步降低声卡支持的采样频率，这将有助于分析低频信号。

“Overload if sample>=”编辑框决定的采样振幅能够激活过载检测机制。

“record from the RECORDER software ring buffer”选项允许从SASLab Pro不支持的设备中录音，例如Acisoft UltraSoundGate、National Instruments DAQ cards。为了使该模式生效，必须选择相关的“RECORDER ring buffer file”，可以通过“ring.wav”按钮或者拖拽到“Sound Card Setting”对话框选择。在录音软件中，the ring buffer必须通过“Monitoring/Ring buffer...”命令设置，并且monitoring必须处于运行状态。
### Playback ![Playback button](playback_button.png)
