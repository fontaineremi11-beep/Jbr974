python
from flask import Flask, render _template,
request, jsonify
app = Flask (_ name_)
# Base simple de réponses
knowledge_base = {
"html": "HTML est le langage de base
pour structurer les pages web.",
"css": "CSS sert à styliser les pages web, pour gérer les couleurs, polices, mise en page.",
"javascript": "JavaScript permet de
rendre les pages web interactives.",
"comment créer un bouton": "Voici un
exemple de bouton HTML : <button>Cliquez-moi</button›",
"comment ajouter une image": "Pour
ajouter une image : <img
src='url de_l_image' alt='description' /›",
"frameworks css": "Les frameworks populaires sont Bootstrap, Tailwind Css,
Bulma.",
Capp.route ("/")
def index () :
return render_template ("index.html")

@app. route ("'/")
def index () :
return render_template ("index.html")
@app.route ("/ask", methods=["POST"'])| def ask ():
question = request.json.get ("question",
""') . lower ()
for key in knowledge_base:
if key in question:
return jsonify({"answer":
knowledge_base [key] })
return jsonify({"answer": "Désolé, je n'ai pas la réponse à cette question pour le moment. "})
if name_ == " main
app. run (debug=True)
" :
