- **Type of Modules**
  - **Auxiliary**
    - Any supporting module, such as scanners, crawlers, and fuzzers, can be found here.

      ```bash
      root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 auxiliary/
      auxiliary/
      ├── admin
      ├── analyze
      ├── bnat
      ├── client
      ├── cloud
      ├── crawler
      ├── docx
      ├── dos
      ├── example.py
      ├── example.rb
      ├── fileformat
      ├── fuzzers
      ├── gather
      ├── parser
      ├── pdf
      ├── scanner
      ├── server
      ├── sniffer
      ├── spoof
      ├── sqli
      ├── voip
      └── vsploit

      20 directories, 2 files
      ```

      `port scan`

  - **Encoders**
    - Encoders will allow you to encode the exploit and payload in the hope that a signature-based antivirus solution may miss them.

      ```bash
      root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 encoders/
      encoders/
      ├── cmd
      ├── generic
      ├── mipsbe
      ├── mipsle
      ├── php
      ├── ppc
      ├── ruby
      ├── sparc
      ├── x64
      └── x86

      10 directories, 0 files
      ```

  - **Evasion**
    - While encoders will encode the payload, they should not be considered a direct attempt to evade antivirus software. On the other hand, "evasion" modules will try that, with more or less success.

      ```bash
      root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 2 evasion/
      evasion/
      └── windows
          ├── applocker_evasion_install_util.rb
          ├── applocker_evasion_msbuild.rb
          ├── applocker_evasion_presentationhost.rb
          ├── applocker_evasion_regasm_regsvcs.rb
          ├── applocker_evasion_workflow_compiler.rb
          ├── process_herpaderping.rb
          ├── syscall_inject.rb
          ├── windows_defender_exe.rb
          └── windows_defender_js_hta.rb

      1 directory, 9 files
      ```

  - **Exploits**
    - Exploits, neatly organized by target system.

      ```bash
      root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 exploits/
      exploits/
      ├── aix
      ├── android
      ├── apple_ios
      ├── bsd
      ├── bsdi
      ├── dialup
      ├── example_linux_priv_esc.rb
      ├── example.py
      ├── example.rb
      ├── example_webapp.rb
      ├── firefox
      ├── freebsd
      ├── hpux
      ├── irix
      ├── linux
      ├── mainframe
      ├── multi
      ├── netware
      ├── openbsd
      ├── osx
      ├── qnx
      ├── solaris
      ├── unix
      └── windows

      20 directories, 4 files
      ```

  - **NOPs**
    - NOPs (No OPeration) do nothing, literally. They are often used as a buffer to achieve consistent payload sizes.

      ```bash
      root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 nops/
      nops/
      ├── aarch64
      ├── armle
      ├── cmd
      ├── mipsbe
      ├── php
      ├── ppc
      ├── sparc
      ├── tty
      ├── x64
      └── x86

      10 directories, 0 files
      ```

  - **Payloads**
    - Payloads are codes that will run on the target system.

      ```bash
      root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 payloads/
      payloads/
      ├── adapters
      ├── singles
      ├── stagers
      └── stages

      4 directories, 0 files
      ```

      - **Adapters** - Wraps single payload to convert them into different adapters. e.g., PowerShell/cmd…
      - **Singles** - Self-contained payloads (add user, launch notepad.exe, etc.) that do not need to download an additional component to run.
      - **Stagers** - Responsible for setting up a connection channel between Metasploit and the target system. Useful when working with staged payloads.
      - **Stages** - Downloaded by the stager. This will allow you to use larger sized payloads.

  - **Post**
    - Post modules will be useful on the final stage of the penetration testing process listed above, post-exploitation.

      ```bash
      root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 post/
      post/
      ├── aix
      ├── android
      ├── apple_ios
      ├── bsd
      ├── firefox
      ├── hardware
      ├── linux
      ├── multi
      ├── networking
      ├── osx
      ├── solaris
      └── windows

      12 directories, 0 files
      ```
