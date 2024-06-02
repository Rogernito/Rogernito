from docx import Document
from docx.shared import Pt, RGBColor
from docx.enum.text import WD_PARAGRAPH_ALIGNMENT

# Create a new Document
doc = Document()

# Title Section
title_section = doc.add_paragraph()
title_section.alignment = WD_PARAGRAPH_ALIGNMENT.CENTER

# Add the first line (names)
names = title_section.add_run("DEWASME PAULIN, GAËTAN, DEVOS MATHÉO, DEGROTE ANTOINE")
names.font.size = Pt(14)
names.bold = True

# Add the school name
school_name = title_section.add_run("\nHaute École Léonard de Vinci")
school_name.font.size = Pt(12)
school_name.bold = True

# Add a placeholder for the logo
logo_placeholder = title_section.add_run("\n[LOGO]")
logo_placeholder.font.size = Pt(12)
logo_placeholder.italic = True

# Add the project code and title
project_code = title_section.add_run("\n\nEPSV-3130-PROJET 2")
project_code.font.size = Pt(14)
project_code.bold = True

project_title = title_section.add_run("\n\n\"Rendez-vous en terre inconnue\"")
project_title.font.size = Pt(12)
project_title.italic = True

# Add the academic year
academic_year = title_section.add_run("\n\n2023/2024")
academic_year.font.size = Pt(12)
academic_year.bold = True

# Add the group information
group_info = title_section.add_run("\n\nGROUPE 1")
group_info.font.size = Pt(12)
group_info.bold = True

# Add the names of the group members
group_members = title_section.add_run("\n\nDENIS MATHIEU, ROBBENS DIDIER, PANEPINTO GINO, PECORARO STÉFANO")
group_members.font.size = Pt(12)
group_members.bold = True

# Save the document
file_path = "/mnt/data/Document_Esthetique.docx"
doc.save(file_path)

file_path
