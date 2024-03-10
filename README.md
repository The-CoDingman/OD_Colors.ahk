;# OD_Colors.ahk
;Custom Class that allows for recoloring of DropdownLists, ComboBoxes, and ListBoxes in AHK v2

ColorGui := Gui(, "OD_Colors Example")
ColorGui.Add("ComboBox", "w300 +0x210 vComboBox1", ["ComboBox Item #1", "ComboBox Item #2", "ComboBox Item #3"])
OD_Colors.Attach(ColorGui["ComboBox1"], Map("T", 0xFFFFFF, "B", 0x0000FF))

OD_Colors.SetItemHeight("s40", "Helvetica")
MyDDL := ColorGui.Add("DropdownList", "w300 +0x210", ["DDL Item #1", "DDL Item #2", "DDL Item #3"])
OD_Colors.Attach(MyDDL, Map("T", 0x0000FF, "B", 0x666666))

OD_Colors.SetItemHeight("s12", "Helvetica")
ColorGui.Add("ListBox", "w300 +0x50 vListBox1", ["Listbox Item #1", "ListBox Item #2", "ListBox Item #3"])
OD_Colors.Attach(ColorGui["ListBox1"], Map("T", 0x253790, "B", 0x000000))
ColorGui.Show("Center")
