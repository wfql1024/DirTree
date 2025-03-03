# **📂 目录树生成器 (Python)**  

> **✨ 适用于 JetBrains 插件市场的 [TreeInfoTip](https://plugins.jetbrains.com/plugin/XXXXX-treeinfotip) 插件！**  
> 本工具支持 **txt** 和 **markdown** 格式，能够快速生成目录结构，帮助你更好地管理和查看文件系统。

## **🔧 功能特点**
- ✅ **指定根目录**：可自定义需要生成目录树的起始路径。
- ✅ **支持两种输出格式**：纯文本 (`.txt`) 或 Markdown (`.md`)。
- ✅ **自定义过滤规则**：
  - 忽略 **.开头的文件/文件夹**（可选）。
  - 过滤指定的 **文件后缀名**（如 `.pyc`、`.log`）。
  - 过滤特定 **文件夹**（如 `__pycache__`、`dist`）。
- ✅ **适配 JetBrains 插件市场的 `TreeInfoTip` 插件**。

---

## **📌 使用方法**
### **修改脚本文件的入口方法，并执行**
   ```python
  if __name__ == "__main__":
      DirTreeCreator().create_dir_tree()  # 无参构造，使用的配置文件在脚本同目录
  
      # # 有参构造，可以使用绝对路径或相对路径
      # DirTreeCreator(fr'D:\SpaceDev\MyProj\MultiWeChatManager\.scripts\dir_tree_config.xml').create_dir_tree()
   ```
- 效果见附录
---

## **🛠 配置项说明**
脚本文件通过xml加载 **自定义配置**，可以通过 `tree_config.xml` 进行修改，里面已经写好注释

---

## **📞 联系方式**
如果你有任何问题或建议，欢迎提交 Issue 或 PR！  
加V：**wfql1024**

## **🚀 支持作者**
![rewards](https://github.com/user-attachments/assets/9a632a23-69f2-4e80-b207-ca9d98f00ba9)

---

## 附录：效果示例
### 场景1：生成本项目的目录数
- 以下是本项目的目录结构示例：
  ```
  📁 项目根目录
  ├─📄 create_dir_tree.py
  ├─📄 DirectoryV3.xml
  ├─📄 dir_tree.txt
  └─📄 tree_config.xml-----#目录树生成配置
  ```
### 场景2：生成其他项目的目录数
  ```python
  if __name__ == "__main__":
      # DirTreeCreator().create_dir_tree()  # 无参构造，使用的配置文件在脚本同目录
  
      # 有参构造，可以使用绝对路径或相对路径
      DirTreeCreator(fr'D:\SpaceDev\MyProj\MultiWeChatManager\.scripts\dir_tree_config.xml').create_dir_tree()
   ```
  - 生成的MultiWeChatManager项目的目录树：
  ```
  ├─📁 decrypt----------------------#解密方法
  │ ├─📁 impl
  │ │ ├─📄 WeChat_decrypt_impl.py
  │ │ └─📄 Weixin_decrypt_impl.py
  │ ├─📄 interface.py
  │ └─📄 __init__.py
  ├─📁 Demo-------------------------#与项目相关的独立示例代码，可以探索下
  │ ├─📁 close_wechat_mutex
  │ ├─📁 debug
  │ ├─📁 decrypt
  │ ├─📁 dll_injection
  │ ├─📁 dll_modify
  │ ├─📁 github_download
  │ ├─📁 hwnd
  │ └─📁 mutex
  ├─📁 external_res-----------------#引用到的外部资源
  │ ├─📄 handle.exe
  │ ├─📄 path.ini
  │ ├─📄 rewards.png
  │ ├─📄 SunnyMultiWxMng.ico
  │ ├─📄 sy.ini
  │ ├─📄 Updater.exe
  │ ├─📄 wechat-dump-rs.exe
  │ ├─📄 WeChatMultiple_Anhkgg.exe
  │ └─📄 WeChatMultiple_lyie15.exe
  ├─📁 functions--------------------#功能层代码，实现项目中的具体功能
  │ ├─📄 func_account.py
  │ ├─📄 func_config.py
  │ ├─📄 func_detail.py
  │ ├─📄 func_file.py
  │ ├─📄 func_hotkey.py
  │ ├─📄 func_login.py
  │ ├─📄 func_setting.py
  │ ├─📄 func_sw_dll.py
  │ ├─📄 func_update.py
  │ ├─📄 subfunc_file.py------------#subfunc为介于工具类和功能直接实现类的子功能类
  │ ├─📄 subfunc_sw.py--------------#平台相关的子功能类
  │ └─📄 __init__.py
  ├─📁 public_class-----------------#公用的类
  │ ├─📄 enums.py
  │ ├─📄 global_members.py----------#作用全局的成员
  │ ├─📄 reusable_widget.py---------#可复用的控件
  │ └─📄 __init__.py
  ├─📁 resources--------------------#项目代码资源
  │ ├─📄 config.py
  │ ├─📄 constants.py
  │ ├─📄 strings.py
  │ └─📄 __init__.py
  ├─📁 ui---------------------------#界面层代码，实现界面创建和更新
  │ ├─📄 about_ui.py
  │ ├─📄 acc_manager_ui.py
  │ ├─📄 acc_tab_ui.py
  │ ├─📄 classic_row_ui.py
  │ ├─📄 debug_ui.py
  │ ├─📄 detail_ui.py
  │ ├─📄 loading_ui.py
  │ ├─📄 main_ui.py
  │ ├─📄 menu_ui.py
  │ ├─📄 rewards_ui.py
  │ ├─📄 setting_ui.py
  │ ├─📄 sidebar_ui.py
  │ ├─📄 statistic_ui.py
  │ ├─📄 treeview_row_ui.py
  │ ├─📄 update_log_ui.py
  │ └─📄 __init__.py
  ├─📁 utils------------------------#工具类代码，可移植到其他项目中使用
  │ ├─📄 debug_utils.py
  │ ├─📄 file_utils.py
  │ ├─📄 handle_utils.py
  │ ├─📄 hwnd_utils.py
  │ ├─📄 image_utils.py
  │ ├─📄 ini_utils.py
  │ ├─📄 json_utils.py
  │ ├─📄 logger_utils.py
  │ ├─📄 memory_utils.py
  │ ├─📄 patch_utils.py
  │ ├─📄 process_utils.py
  │ ├─📄 pywinhandle.py
  │ ├─📄 string_utils.py
  │ ├─📄 sw_utils.py
  │ ├─📄 sys_utils.py
  │ ├─📄 widget_utils.py
  │ └─📄 __init__.py
  ├─📄 Build4Win10+.bat
  ├─📄 Build4Win7.bat
  ├─📄 click_me_to_create_lnk.bat---#已不再维护，留个念想
  ├─📄 DirectoryV3.xml
  ├─📄 main.py----------------------#入口，管理员身份及程序参数解析
  ├─📄 README.md
  ├─📄 remote_setting---------------#加密的云端配置源
  ├─📄 requirements.txt
  ├─📄 update_program.py------------#升级器
  ├─📄 version_adaptation.json------#版本适配表，在这里更新微信新版本的偏移地址，2.5及之前可用
  └─📄 version_config.json----------#旧的版本适配表，只在发布过的2.3.3.333可以使用，现在代码已经不使用
  ```

---
## **🛠 配置项说明**
脚本文件通过xml加载 **自定义配置**，可以通过 `tree_config.xml` 进行修改，里面已经写好注释

---

## **📞 联系方式**
如果你有任何问题或建议，欢迎提交 Issue 或 PR！  
加V：**wfql1024**

## **🚀 支持作者**
![rewards](https://github.com/user-attachments/assets/9a632a23-69f2-4e80-b207-ca9d98f00ba9)