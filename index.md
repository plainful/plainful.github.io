---
layout: page  
title: 欢迎来到我的博客
---

- 姓名：杨佳昊
- 学号：125090830

![我的照片](/images/屏幕截图 2025-09-02 175737.jpg)

- 附加题代码：
  import pdfplumber

  pdf_path = r"C:\Users\23993\Downloads\2024年学生IT手册.pdf"  # 本地文件路径
  markdown_path = "output.md"  # 输出的 Markdown 文件名

  def pdf_to_markdown(pdf_path, markdown_path):
      with pdfplumber.open(pdf_path) as pdf:
          markdown_content = ""
          for page in pdf.pages:
              text = page.extract_text()
              if text:
                  markdown_content += text + "\n\n"
    
      with open(markdown_path, 'w', encoding='utf-8') as f:
          f.write(markdown_content)
    
      print(f"✅ 转换完成！Markdown 文件已保存为: {markdown_path}")

  # 执行转换
  pdf_to_markdown(pdf_path, markdown_path)

