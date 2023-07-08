"""Boilerplate for PySide based GUI. With some limitation, it can be run outside of Houdini"""

import importlib.util
import os, sys

HOUDINI_CALL = False

if importlib.util.find_spec("hou") is None:
    from PySide6 import QtWidgets, QtGui, QtCore, QtUiTools
else:
    from PySide2 import QtWidgets, QtGui, QtCore, QtUiTools
    import hou
    HOUDINI_CALL = True


class MyWindow(QtWidgets.QMainWindow):
	def __init__(self, parent=None):
		super(MyWindow, self).__init__(parent)
		file_interface = os.path.join(MAIN_UI_PATH")
		self.ui = QtUiTools.QUiLoader().load(file_interface, parentWidget=self)
		self.setWindowTitle("NAME")
		if HOUDINI_CALL:
			stylesheet = hou.qt.styleSheet()
			self.setStyleSheet(stylesheet)
		

#Create UI Window
if HOUDINI_CALL:

		
	my_window = MyWindow()
	my_window.show()

else:
	if __name__ == '__main__':
		app = QtWidgets.QApplication([])
		fb = MyWindow()
		fb.show()
		app.exec()
