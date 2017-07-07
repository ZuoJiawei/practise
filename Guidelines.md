# Useful links
- [Wuhan Site Information Center](https://sp-fin/sites/wuhan/Shared%20Documents/Forms/AllItems.aspx)

    Contains almost all common documentation you may need in Wuhan site.

- [Wuhan ETF](https://sp-ig/sites/sef/WHef/Shared%20Documents/Forms/AllItems.aspx)
    
    Wuhan Engineering Technical Forum

- [Synopsys World](https://synopsysworld/Pages/home.aspx)
- [Employee Central](http://myec)
- [IT Web](https://itweb/Pages/home.aspx)
- [Timesheet, need to fill in every week](https://us02vwepmapps//sts/index.aspx)

- [ARC SW Wiki](https://sp-sg/sites/arc-sw/Wiki/Home.aspx)

    SNPS ARC Software Team wiki
    
- [ARC Open Source Organization](https://github.com/foss-for-synopsys-dwc-arc-processors)
  - embARC Related
    - [embARC OSP](https://github.com/foss-for-synopsys-dwc-arc-processors/embarc_osp)
    - [embARC Applications](https://github.com/foss-for-synopsys-dwc-arc-processors/embarc_applications)
    - [embARC Website](http://embarc.org/)

- [ARC Tools&IP Release StagingArea](http://arcprojects/mnt/StagingArea/)

    Mainly for us to download tools.
    
# Tools need to be installed
- [Metaware Toolset](http://arcprojects/mnt/StagingArea/arc_MWDT_ARC/)
	-  *Note*: Before you tap make in cmd line,be sure that the License is added into the environment variables list.[Click here](https://msdn.microsoft.com/en-us/library/windows/desktop/ms682653(v=vs.85).aspx) to find out how to operate with your PC. 
- [Metaware nSIM](http://arcprojects/mnt/StagingArea/arc_nSIM/)
- [ARC GNU Toolset](https://github.com/foss-for-synopsys-dwc-arc-processors/toolchain/releases)
- [Cygwin](https://www.cygwin.com/)
  - [apt-cyg](https://github.com/transcode-open/apt-cyg)
  - [chere](https://cygwin.com/cgi-bin2/package-cat.cgi?file=x86%2Fchere%2Fchere-1.3-1&grep=chere)
- [Virtual Box](http://www.virtualbox.org/)
  - Debian/Ubuntu/Centos etc

# Product Documentation Reference
- [ARC Cores](https://spp/pic/dw/Pages/ARC.aspx)
- [Find System of SNPS](http://find/)

# Hardwares we used in development
- [EM Starter Kit](http://arcprojects/mnt/StagingArea/ARC_EM_Starter_Kit/)
- HSDK
- EMDK
- HuangShan II IC
- [AXS 103](http://arcprojects/mnt/StagingArea/ARC_Software_Development_Platform_axs103/)
- [Arduino 101](https://github.com/01org/corelibs-arduino101)
- [Sensor Subsystem](http://arcprojects/mnt/StagingArea/arc_sensor_subsystem/)
- [Data Fusion Subsystem](http://arcprojects/mnt/StagingArea/arc_datafusion_subsystem/)

# embARC Team responsibility
- embARC OSP, embARC BSP, embARC APP
  - OSP: Open Software Platform
  - BSP: Board Support Package
  - APP: Application
- Zephyr, FreeRTOS, LiteOS, Openthread, Contiki, RIOT, Toppers and MyNewt Upstream

# Skills need to master
- Source Code Control: Git, P4
  - Git Frontends
    - [SourceTree APP](http://sourcetreeapp.com/)
	    - *Note*: SourceTree App requires you to sign in an account which can't be resolved until you have vpn to surf net out of the **WALL**.
    - [Tortoise Git](https://tortoisegit.org/)
	    - *Note*: Before installing tortoise you should first download [git bash](https://git-scm.com/downloads).
- Development Environment: Windows, Linux
- Document Language: Markdown
	- *Note* Markdown is a powerful html script language,tutorials are available [here](http://www.jianshu.com/p/20e82ddb37cb) ,and [online markdown notepad](https://maxiang.io/),[For Offline Note: MarkdownPad2](http://markdownpad.com/download.html)
- Script Language: Makefile, Shell, Python, Javascript
	- makefile tutorials:[Hao Chen](http://wiki.ubuntu.org.cn/%E8%B7%9F%E6%88%91%E4%B8%80%E8%B5%B7%E5%86%99Makefile:MakeFile%E4%BB%8B%E7%BB%8D)
	- python tutorials:[Python 27 For Beginners,Mooc](http://www.imooc.com/learn/177), or [Xuefeng Liao's tutorial](http://www.liaoxuefeng.com/wiki/001374738125095c955c1e6d8bb493182103fac9270762a000/)
- CI tools: Jenkins
- Prefer Editors
  - Sublime Text
    - [Package Control](https://packagecontrol.io/)
    - [CTags](https://packagecontrol.io/packages/CTags)
	    - *Note*: You should first install ctags package using sublime's package control panel.
    	- *Note*: Attention:If you want to use ctag to locate where varibles are defined,you should download [catgs](http://ctags.sourceforge.net/)(clike me to download) and paste ctag.exe into sublime's installation directory.
    - [TrailingSpaces](https://packagecontrol.io/packages/TrailingSpaces)
    - [SideBarEnhancements](https://packagecontrol.io/packages/SideBarEnhancements)
    - [ConvertToUTF8](https://packagecontrol.io/packages/ConvertToUTF8)
    - [SublimeAStyleFormatter](https://packagecontrol.io/packages/SublimeAStyleFormatter)
  - ATOM or VSCode
  - Notepad ++
  - Vim or Emacs for Linux Command Line
- Perfer COM/UART Terminal
  - Windows: Putty, Teraterm
  - Linux: Putty, minicom, ckermit

