# Qiskit Installation
 Welcome to EE405A. During the first 4 weeks, we are going to cover the theory and practical use of quantum computation. From the second lecture, we will utilize Qiskit to implement a quantum circuit and to simulate a quantum computer.
  Qiskit is an open-source framework for working with quantum computers provided by IBM. You can build a quantum algorithm and run it not only by simulation on your desktop but also by a real quantum machine on the q-experience cloud in IBM. More information is available at [https://github.com/Qiskit/qiskit](https://github.com/Qiskit/qiskit).
 This document is about the installation and configuration of Anaconda and Qiskit. Recommended OSs are as below :
  - Ubuntu >=16.04
  - MAC os >=10.12.6
  - Windows >= 7
 
## 1. Anaconda Installation
 1. Go to [https://www.anaconda.com/distribution/](https://www.anaconda.com/distribution/).
 2. Select your OS and install Anaconda with python version of >=3.7.

## 2. Anaconda Configuration
 1. Open Anaconda Navigator, and click Environments in the left sidebar.
 2. Click the Create button and make your environment with any name you want (for example, "qiskit_env", "qiskit_venv"...). Make sure the python version of 3.7 in the pop-up.
3. **(Ubuntu/Mac)** Open a terminal and check if there is (base) or (your_env) at the start of the line. 
  - If not, copy and paste the following code at the end of the file `~/.bashrc`(Ubuntu) or `~/.bash_profile`(Mac). And then, check it after restarting the terminal.

```bash
  # added by Anaconda3 2019.10 installer
# >>> conda init >>>
# !! Contents within this block are managed by 'conda init' !!
__conda_setup="$(CONDA_REPORT_ERRORS=false '/Users/leegwonhak/opt/anaconda3/bin/conda' shell.bash hook 2> /dev/null)"
if [ $? -eq 0 ]; then
    \eval "$__conda_setup"
else
    if [ -f "/Users/leegwonhak/opt/anaconda3/etc/profile.d/conda.sh" ]; then
# . "/Users/leegwonhak/opt/anaconda3/etc/profile.d/conda.sh"  # commented out by conda initialize
        CONDA_CHANGEPS1=false conda activate base
    else
        \export PATH="/Users/leegwonhak/opt/anaconda3/bin:$PATH"
    fi
fi
unset __conda_setup
# <<< conda init <<<

# >>> conda initialize >>>
# !! Contents within this block are managed by 'conda init' !!
__conda_setup="$('/Users/leegwonhak/opt/anaconda3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__conda_setup"
else
    if [ -f "/Users/leegwonhak/opt/anaconda3/etc/profile.d/conda.sh" ]; then
        . "/Users/leegwonhak/opt/anaconda3/etc/profile.d/conda.sh"
    else
        export PATH="/Users/leegwonhak/opt/anaconda3/bin:$PATH"
    fi
fi
unset __conda_setup
# <<< conda initialize <<<
```
  
## 3. Qiskit Installation
1. Open a terminal(Ubuntu or Mac) or a Powershell Prompt at the Home in Anaconda Navigator(Windows).
2. Type `pip install qiskit`.
3. You can find the following packages by `conda list | grep qiskit` (`grep` is not working in PowerShell. just type `conda list`)
  - qiskit
  - qiskit-aer
  - qiskit-aqua
  - qiskit-ibmq-provider
  - qiskit-ignis
  - qiskit-terra

4. Then you are ready to use `qiskit`.
