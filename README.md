#
【幸福框架】---【2019】---【GitHub meets you】
-
	-导读
	
	2019年4月26日，在金老师的启发下，我决心认真学习写技术文档。
	认认真真维护一个技术文档，比学什么都快，并且学到更多的知识！
	呼吁朋友们一起来维护这个有趣的技术文档！
	
	这个技术文档的作用：
		1.学习时的帮助文档
		2.学习过程中梳理知识
		3.培养尝试维护一个技术文档的习惯
	
	-导读
#
【1】---【2019.4.26】---【aaapples】--->【今天很勤奋，正能量满满的一天】
-	
	---维护原因
					
	小白进行窗体设计，常遇到问题：
	1.不知道控件长什么样
	2.不知道控件含义
	3.不知道控件常用方法
	
	---维护主体
	
	▣容器：groupBox
	▢：CheckBox
	◯：RadioButton	
	
	【选中】方法：if (c is CheckBox && ((CheckBox)c).Checked == true)
	【遍历】groupBox容器选中的控件：
		    
	foreach (Control b in groupBox2.Controls)
				{
					if (b is RadioButton && ((RadioButton)b).Checked == true)
					{
						// count2 = Convert.ToInt32(b.Text);
					}
				}
				
	---维护主体
#
【1】---【2019.4.27】---【aaapples】--->【实验小结，实战是获取知识最快的方法】
-	
	---维护原因
					
	
	
	---维护主体
	
	刻度尺(滑块的一种)：trackBar
	颜色关键字:Color
	水平滑块：hScrollBar
	▢类似groupbox容器：panel
	文本框：richtextbox	
	
	Color关键字声明颜色变量：
		private Color cl;
		
	显示刻度尺的度：
		label9.Text = trackBar1.Value.ToString()；
		
	显示水平滑块的度：
		label9.Text = hScrollBar1.Value.ToString()；

	颜色设置：
		panel1.BackColor = Color.FromArgb(hScrollBar1.Value, hScrollBar2.Value, hScrollBar3.Value);
			方法：Color.FromArgb(int,int,int);
			(int,int,int):对应颜色的RGB数值，(R,G,B)，最大不超过255
			
		button3.ForeColor = Color.FromArgb(Color.White.R-panel1.BackColor.R, Color.White.G - panel1.BackColor.G, Color.White.B - panel1.BackColor.B);
			提示：R,G，B数值做运算，可得颜色差。
				  每种颜色的RGB数值固定，白色的数值最大，与白色做差运算，颜色取反
				
		string scr = "#" + richTextBox2.ForeColor.R.ToString() + richTextBox2.ForeColor.G.ToString() + richTextBox2.ForeColor.B.ToString();
		private Color cl = System.Drawing.ColorTranslator.FromHtml(scr);	
			把颜色值十六进制转为字符串："#"+"R"+"G"+"B"
			进一步把字符串转为颜色值：System.Drawing.ColorTranslator.FromHtml(scr);
			
		色板控件：colorDialog
			选中颜色判断：
				if(colorDialog1.ShowDialog()==DialogResult.OK)
            {
                button3.BackColor = colorDialog1.Color;
				//ShowDialog()：弹出色板窗口
            }
			
		取消上一次button按钮操作：	
			button1.DialogResult = DialogResult.Cancel;

	
	---维护主体





































