on("chat:message", function (msg) {
    //      Populate all of the potential name variables first
    var     aundarianmalefirst          =   _.sample(["Ari", "Bokk", "Breyten", "Daen", "Dover", "Erben", "Fluin", "Gavrin", "Hagro", "Herschem", "Huys", "Jurian", "Kamiel", "Killian", "Kleris", "Reng", "Retief", "Riaan", "Saal", "Sarelo", "Sithov", "Tak", "Tyman", "Urik"])
    ,       aundarianfemalefirst        =   _.sample(["Aafki", "Agate", "Baltia", "Batrax", "Beleth", "Chantal", "Fientia", "Flerentia", "Gwen", "Hjeltia", "Juliona", "Levini", "Margana", "Marloes", "Sanne", "Sien", "Tanneken", "Vilina"])
    ,       aundarianlast               =   _.sample(["Aarland", "Acker", "Adriansen", "Alyea", "Arendt", "Bacher", "Banekert", "Bartell", "Bateu", "Crudaker", "Caldamus", "Corleis", "Dekker", "Ennes", "Gerlach", "Haldron", "Hugrin", "Jurians", "Karch", "Kendig", "Maartel", "Mantanye", "Merchiot", "Nagel", "Ostren", "Petilom", "Redeker", "Rhuli", "Romhaar", "Serontain", "Shreve", "Sykes", "Taumen", "Thiel", "Toriun", "Tullier", "Valleau", "Veseur", "Yanger", "Zenden"])
    ,       brelishmalefirst            =   _.sample(["Alain", "Beren", "Cord", "Curlot", "Destir", "Duran", "Erix", "Jovi", "Kaine", "Kuven", "Laren", "Lis", "Maal", "Minyu", "Nelt", "Norn", "Oarsen", "Pater", "Pol", "Rand", "Reesir", "Saal", "Stend", "Tars", "Teesen", "Uthar", "Verden", "Vorj", "Werem", "Wrogarr", "Yelfis"])
    ,       brelishfemalefirst          =   _.sample(["Aanna", "Alike", "Beaf", "Channa", "Dabren", "Delru", "Elazti", "Fromm", "Gersi", "Glenas", "Habra", "Heeson", "Isti", "Itlani", "Joherra", "Ket", "Khaal", "Lorsanna", "Margu", "Maril", "Monesti", "Narcy", "Nebra", "Penti", "Riki", "Soranda", "Tabin", "Tolri", "Wroaan", "Wroenna"])
    ,       brelishlast                 =   _.sample(["Aggan", "Bakker", "Colworn", "Devir", "Ebinor", "Faldren", "Graccen", "Helmworth", "Jonz", "Kemble", "Lanner", "Lonn", "Makker", "Morrus", "Nelview", "Perryn", "Riston", "Roole", "Smyth", "Snarik", "Thorn", "Toppe", "Wrighten"])
    ,       karrnathimalefirst          =   _.sample(["Adalstan", "Alarich", "Arend", "Berend", "Brenius", "Detlev", "Drago", "Evetius", "Falko", "Fraedus", "Garrick", "Geroldt", "Gertan", "Gustavus", "Halden", "Leonus", "Leodegar", "Maenrad", "Rochus", "Rolund", "Sigor", "Theoban", "Vedim", "Vorik", "Wultram"])
    ,       karrnathifemalefirst        =   _.sample(["Adalgisa", "Alinda", "Asta", "Bauin", "Clotrila", "Demuth", "Ebba", "Ermena", "Forsindh", "Gisaul", "Harika", "Haedrun", "Karola", "Lorelea", "Mauriana", "Menelda", "Oydelis", "Renilda", "Syardis", "Syele", "Theda", "Valpaea", "Vaunn"])
    ,       karrnathilast               =   _.sample(["Altaner", "Argland", "Balich", "Barthus", "Brand", "Cerfas", "Denka", "Dorn", "Erdei", "Eschus", "Furnau", "Gaebler", "Gergus", "Grogloth", "Hellekanus", "Hintram", "Jaranus", "Karlach", "Kessler", "Kraal", "Lassinus", "Losho", "Maerer", "Ochem", "Rangoth", "Roerith", "Sattler", "Senglin", "Taggert", "Thul", "Trothut", "Vanalan", "Vedenin", "Zecklin"])
    ,       thranemalefirst             =   _.sample(["Alestair", "Arrun", "Andri", "Calemi", "Coref", "Demodir", "Drego", "Drosin", "Egen", "Javi", "Jeffi n", "Kaith", "Lukar", "Mizar", "Ossul", "Pentar", "Rave", "Sercyl", "Sudro", "Suthar", "Syro", "Taran", "Tokorin", "Urdan", "Valtar", "Vencyl", "Verodin", "Zoder"])
    ,       thranefemalefirst           =   _.sample(["Avaliah", "Beref", "Chantalyn", "Draci", "Ghanji", "Hariel", "Heken", "Imperi", "Irulan", "Jahanah", "Kahlia", "Lycia", "Maradal", "Margil", "Melindri", "Morgana", "Narvala", "Norah", "Nyllestra", "Sede", "Suspiria", "Taris", "Thradi", "Varikah"])
    ,       thranelast                  =   _.sample(["Aeyliros", "Askarda", "Atrelioth", "Corliostor", "Corus", "Desekane", "Drosin", "Entarro", "Eskeliendro", "Ghastor", "Hetrion", "Imaradi", "Irvallo", "Karavastar", "Krayci", "Lerendazi", "Marktaros", "Neskus", "Ovion", "Ravadanci", "Sarhain", "Talandro", "Tarravan", "Teskelyndros", "Vanatar", "Vasiraghi"])
    ,       dwarfmalefirst              =   _.sample(["B", "Bal", "Bel", "Bof", "Bol", "D", "Dal", "Dor", "Dw", "Far", "Gil", "Gim", "Kil", "Mor", "Nal", "Nor", "Ov", "Th", "Thor", "Thr"]) +  _.sample(["aim", "ain", "ak", "ar", "i", "im", "in", "o", "or", "ur"])
    ,       dwarffemalefirst            =   _.sample(["B", "Bal", "Bel", "Bof", "Bol", "D", "Dal", "Dor", "Dw", "Far", "Gil", "Gim", "Kil", "Mor", "Nal", "Nor", "Ov", "Th", "Thor", "Thr"]) +  _.sample(["a", "ala", "ana", "ip", "ia", "ila", "ina", "ola", "on", "ona"])
    ,       dwarfclanname               =   _.sample(["Doldarun", "Droranath", "Kolkarun", "d'Kundarak", "Laranak", "Londurak", "Mroranon", "Narathun", "Soldorak", "Soranath", "Toldorath", "Tordannon"])
    ,       elffirstname                =   _.sample(["Adrie", "Ahinar", "Althaea", "Anastrianna", "Andraste", "Antinua", "Arara", "Baelitae", "Bethrynna", "Birel", "Traulam", "Tiaathque", "Thiala", "Theirastra", "Sumnes", "Silaqui", "Shava", "Shanairla", "Sariel", "Ridaro", "Quillathe", "Quelenna", "Naivara", "Myathethil", "Mialee", "Meriele", "Malquis", "Maiathah", "Lia", "Leshanna", "Keyleth", "Jelenneth", "Jarsali", "lrann", "llanis", "lelenia", "Hatae", "Felosial", "Faral", "Enna", "Elama", "Drusilia", "Dara", "Claira", "Chaedi", "Caelynn", "Vadania", "VaIanthe", "Xanaphia", "Adran", "Aelar", "Aerdeth", "Ahvain", "Aramil", "Arannis", "Aus", "Azaki", "Beiro", "Berrian", "Caeldrim", "Carrie", "Dayereth", "Dreali", "Efferil", "Eiravel", "Enialis", "Erdan", "Erevan", "Fivin", "Galinndan", "Gennal", "Hadarai", "Halimath", "Heian", "Himo", "lmmeral", "lvellios", "Korfel", "Lamlis", "Laucian", "Lucan", "Mindartis", "Naal", "Nutae", "Paelias", "Peren", "Quarion", "Riardon", "Rolen", "Soveliss", "Suhnae", "Thamior", "Tharivol", "Theren", "Theriatis", "Thervan", "Uthemar", "Vanuath", "Varis"])
    ,       elflastname                 =   _.sample(["Aloro", "Amakiir", "Amastacia", "Ariessus", "Arnuanna", "Berevan", "Caerdonel", "Caphaxath", "Casilltenirra", "Cithreth", "Dalanthan", "Eathalena", "Erenaeth", "Ethanasath", "Fasharash", "Firahel", "Floshem", "Galanodel", "Goltorah", "Hanali", "Holimion", "Horineth", "lathrana", "llphelkiir", "lranapha", "Koehlanna", "Lathalas", "Liadon", "Meliamne", "Mellerelel", "Mystralath", "Nailo", "Netyoive", "Ofandrus", "Ostoroth", "Othronus", "Qualanthri", "Raethran", "Rothenel", "Selevarun", "Siannodel", "Suithrasas", "Sylvaranth", "Teinithra", "Tiltathana", "Wasanthi", "Withrethin", "Xiloscient", "Xistsrith", "Yaeldrin"])
    ,       gnomemalefirst              =   _.sample(["Alston", "Alvyn", "Anverth", "Arumawann", "Bilbron", "Boddynock", "Broce", "Burgell", "Cockaby", "Crampernap", "Dabbledob", "Delebean", "Eberdeb", "Eldon", "Erky", "Fabien", "Fibblestib", "Fonkin", "Frouse", "Frug", "Gerbo", "Gimble", "Glim", "lgden", "Jabbie", "Jebeddo", "Kellen", "Kipper", "Namfoodle", "Oppleby", "Orryn", "Paggen", "Pallabar", "Pog", "Qualen", "Ribbles", "Rimple", "Roondar", "Sapply", "Seebo", "Senteq", "Sindri", "Umpen", "Warryn", "Wiggens", "Wiggens", "Wobbles", "Wrenn", "Zaffrab", "Zook"])
    ,       gnomefemalefirst            =   _.sample(["Albaratie", "Bafflestone", "Beren", "Boondiggles", "Cobblelob", "Daergel", "Fabblestabble", "Dunben", "Fapplestamp", "Fiddlefen", "Folkor", "Garrick", "Gimlen", "Glittergem", "Gobblefirn", "Gummen", "Horcusporcus", "Humplebumple", "lronhide", "Leffery", "Lingenhall", "Loofollue", "Maekkelferce", "Miggledy", "Munggen", "Murnig", "Musgraben", "Nackle", "Ningel", "Nopenstallen", "Nucklestamp", "Offund", "Oomtrowl", "Pilwicken", "Pingun", "Quillsharpener", "Raulnor", "Reese", "Rofferton", "Scheppen", "Shadowcloak", "Silverthread", "Sympony", "Tarkelby", "Timbers", "Turen", "Umbodoben", "Waggletop", "Welber", "Wildwander"])
    ,       gnomelast                   =   _.sample(["Abalaba", "Bimpnottin", "Breena", "Buvvie", "Caramip", "Callybon", "Carlin", "Cumpen", "Dalaba", "Donella", "Duvamil", "Ella", "Ellyjoybell", "Ellywick", "Enidda", "Lilli", "Loopmottin", "Lorilla", "Luthra", "Mardnab", "Meena", "Menny", "Mumpena", "Nissa", "Numba", "Nyx", "Oda", "Oppah", "Orla", "Panana", "Pyntle", "Quilla", "Ranala", "Reddlepop", "Roywyn", "Salanop", "Shamil", "Siffress", "Symma", "Tana", "Tenena", "Tervaround", "Tippletoe", "Ulla", "Unvera", "Veloptima", "Virra", "Waywocket", "Yebe", "Zanna"])
    ,       halflingmalefirst           =   _.sample(["Alton", "Ander", "Bernie", "Bobbin", "Cade", "Callus", "Corrin", "Dannad", "Danniel", "Eddie", "Egart", "Eldon", "Errich", "Fildo", "Finnan", "Franklin", "Garret", "Garth", "Gilbert", "Gob", "Harol", "Igor", "Jasper", "Keith", "Kevin", "Lazam", "Lerry", "Lindal", "Lyle", "Merrie", "Mican", "Milo", "Morrin", "Nebin", "Nevil", "Osborn", "Oswalt", "Perrin", "Poppy", "Reed", "Roscoe", "Sam", "Shardon", "Tye", "Ulmo", "Wellby", "Wendel", "Wenner", "Wes"])
    ,       halflingfemalefirst         =   _.sample(["Alain", "Andry", "Anne", "Bella", "Blossom", "Bree", "Callie", "Chenna", "Cora", "Dee", "Dell", "Eida", "Eran", "Euphemia", "Georgina", "Gynnie", "Harriet", "Jasmine", "Jillian", "Jo", "Kithri", "Lavinia", "Lidda", "Maegan", "Marigold", "Merla", "Myria", "Nedda", "Nikki", "Nora", "Olivia", "Paela", "Pearl", "Pennie", "Philomena", "Portia", "Robbie", "Rose", "Sarai", "Seraphina", "Shaena", "Stacee", "Tawna", "Thea", "Trym", "Tyna", "Vani", "Verna", "Wella", "Willow"])
    ,       halflinglast                =   _.sample(["Appleblossom", "Bigheart", "Brightmoon", "Brushgather", "Cherrycheeks", "Copperkettle", "Deephollow", "Deephollow", "Elderberry", "Fastfoot", "Fatrabbit", "Glenfellow", "Goldfound", "Goodbarrel", "Goodearth", "Greenbottle", "Greenleaf", "High-hill", "Hilltopple", "Hogcollar", "Honeypot", "Jamjar", "Kettlewhistle", "Leagallow", "Littlefoot", "Nimblefingers", "Porridgepot", "Quickstep", "Reedfellow", "Shadowquick", "Silvereyes", "Smoothhands", "Stonebridge", "Stoutbridge", "Stoutman", "Strongbones", "Sunmeadow", "Swiftwhistle", "Tallfellow", "TeaPenny", "Thistletop", "Thorngage", "Tosscobble", "Underbough", "Underfoot", "Warmwater", "Whispermouse", "Wildcloak", "Wildheart", "Wiseacre"])
    ,       orcfirst                    =   _.sample(["Nar", "Gun", "Rall", "Brar", "Brugvun", "Gruddakk", "Dudral", "Jortukk", "Brutran", "Zhutag", "Ghun", "Vin", "Rhuk", "Rhuam", "Bellul", "Bhivgon", "Ovie", "Rhivnuf", "Ilvo", "Movo", "Buk", "Zhukk", "Zok", "Lar", "Lanzan", "Rharlor", "Rhardon", "Zhobrok", "Bhurlur", "Urlok", "Dheng", "Beef", "Nuz", "Nev", "Ova", "Kongiz", "Aovno", "Guthao", "Kegvo", "Angok", "Gub", "Shak", "Guk", "Ghakk", "Aggukk", "Drugvakk", "Zartakk", "Ganall", "Nugak", "Guhzan", "Crogzakh", "Gholcmac", "Srulfod", "Druhol", "Shauhaud", "Aulgi", "Aufdaukh", "Agzec", "Uddol", "Ozgaul", "Defdokh", "Mirzidh", "Sruglil", "Srecrigh", "Gracrauc", "Arderg", "Uzrokh", "Ugakh", "Odbosh", "Acbol", "Ghagzil", "Lorzudh", "Gaucbo", "Shoddit", "Soggo", "Acrirg", "Uzzuc", "Ashnog", "Olcmokh", "Auhoc", "Buthru", "Cuhirg", "Krugif", "Brogzagh", "Silcmer", "Afdoc", "Auggaudh", "Aucdegh", "Uldaugh", "Aulget", "Grauthri", "Cigzag", "Droftheg", "Suthro", "Racdo", "Auglu", "Olcmol", "Aushnuf", "Agridh", "Othred", "Cregesh", "Shuthruc", "Rezgef", "Dracrash", "Dauzzash", "Auzro", "Oddot", "Orzig", "Audbe", "Ashnul", "Rolderg", "Lishne", "Merdagh", "Bocro", "Shathrul", "Azgith", "Ugrug", "Odbul", "Augokh", "Oddad", "Giftha", "Ruzrat", "Srirbaukh", "Gulcmol", "Drolfel", "Uggar", "Ugduth", "Uzbegh", "Orco", "Azbo", "Saglash", "Kreddut", "Brugdeth", "Crardal", "Rarbi", "Ashnir", "Aulgor", "Authrirg", "Aurcel", "Urzug", "Loglid", "Kaugikh", "Sracdegh", "Druzugh", "Grirzuf", "Augbakh", "Aushnig", "Ahug", "Agdot", "Urgu"])
    ,       orclast                     =   _.sample(["", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "Toe Spear", "Chin Shatterer", "Giant Trasher", "Storm Killer", "Brass Hammer", "Nose Gouger", "Teeth Strangler", "Flesh Strangler", "Brain Scalper", "Nose Smasher", "The Fearless", "The Butcher", "The Smug", "Death Cutter", "The Vivid", "Rib Flayer", "The Crazy", "The Violent", "The Prime", "The Crooked", "The Disfigured", "Slave Wrecker", "The Fierce", "The Cold", "The Enormous", "The Outlandish", "Scale Cleaver", "Blood Quasher", "Spite Mutilator", "Doom Sword", "Eye Gouger", "Iron Mutilator", "The Ugly", "The Volatile", "Brain Masher", "Vein Slicer", "The Broad", "The Colossal", "The Barbarian", "Dream Cleaver", "Feet Ripper", " The Barbarian", "Ash Pummel", "Thunder Strangler", "The Brutal", "The Colossal", "Ankle Masher", "The Ugly", "The Warped", "The Infernal"])
	,		gnollfirst					=	_.sample(["Abark", "Abral", "Adrokh", "Adruth", "Aldel", "Aldem", "Althag", "Ammakh", "Anrod", "Ardakh", "Arog", "Arthat", "Asmud", "Ebrot", "Edak", "Edneth", "Edrark", "Elab", "Elbog", "Eldeth", "Eldok", "Eltheg", "Errek", "Erthoth", "Esmad", "Esmur", "Eyohk", "Ideb", "Idrat", "Igrel", "Ildud", "Ileth", "Iltek", "Ilthalk", "Ilthel", "Indor", "Inrurk", "Irak", "Irbeth", "Irdag", "Irrat", "Irtel", "Ismeth", "Iteg", "Obreth", "Ognerk", "Ognoth", "Olthot", "Onrur", "Orteth", "Orthod", "Ortum", "Othot", "Ubath", "Ubroth", "Ubuk", "Udrukh", "Ular", "Ulath", "Ulgud", "Ultak", "Umdath", "Umnod", "Undal", "Urdot", "Urgam", "Urtor", "Usmog", "Usner", "Uthur"])
	,		goblinfirst					=	_.sample(["Zrak", "Zadar", "Vrak", "Val", "Uron", "Nuk", "Nen", "Muv", "Marg", "Lok", "Lod", "Krag", "Khol", "Khek", "Kan", "Grel", "Grek", "Gag", "Drog", "Dograg"])
	,		hobgoblinfirst				=	_.sample(["Akreg", "Averz", "Daldravod", "Derbanurz", "Drogreg", "Drondrurz", "Egrud", "Evredor", "Gezrur", "Gloldranar", "Gluvlanur", "Grakkuc", "Grel", "Groldrar", "Gulvrug", "Kheldrac", "Khovrol", "Klorburog", "Klurarz", "Kognurz", "Mulvoc", " Muvrarg", " Muvreg", "Nukvor", "Rogroc", "Uvrek", "Valzar", "Vekroduk", "Vozul", " Vrokverg", "Vroldrorud", "Zrakron", "Zrulvrok"])
	,		warforgedfirst				=	_.sample(["Unmaker", "Two", "Titan", "Three", "Ten", "Stitcher", "Sprite", "Sparkle", "Six", "Shielder", "Seven", "Senser", "Scorcher", "Salvager", "Sabre", "One", "Nurse", "Nine", "Murderer", "Marker", "Leaper", "Knocker", "Knife", "Killer", "Jury", "Iron", "Inspector", "Heart", "Glaive", "Gasher", "Friend", "Four", "Five", "Fire", "Falchion", "Etcher", "Epee", "Enchanter", "Eleven", "Eight", "Driver", "Drifter", "Dreamer", "Delver", "Dealer", "Curator", "Crumbler", "Creese", "Coil", "Clubber", "Chopper", "Chaser", "Chain", "Catcher", "Carriage", "Calmer", "Booster", "Author", "Aegis", "Twelve"])
	,       halforcmalefirst            =   _.sample([aundarianmalefirst.concat(brelishmalefirst.concat(karrnathimalefirst.concat(thranemalefirst.concat(orcfirst))))])
    ,       halforcfemalfirst           =   _.sample([aundarianfemalefirst.concat(brelishfemalefirst.concat(karrnathifemalefirst.concat(thranefemalefirst.concat(orcfirst))))])
    ,       halforclast                 =   _.sample([aundarianlast.concat(brelishlast.concat(karrnathilast.concat(thranelast.concat(orclast))))])
    ,       halfelfmalefirst            =   _.sample([aundarianmalefirst.concat(brelishmalefirst.concat(karrnathimalefirst.concat(thranemalefirst.concat(elffirstname))))])
    ,       halfelffemalfist            =   _.sample([aundarianfemalefirst.concat(brelishfemalefirst.concat(karrnathifemalefirst.concat(thranefemalefirst.concat(elffirstname))))])
    ,       halfelflast                 =   _.sample([aundarianlast.concat(brelishlast.concat(karrnathilast.concat(thranelast.concat(elflastname))))])
    ,       randrace                    =   ["aundarian","brelish","karrnathi","thrane","dwarf","elf","gnome","halfling","orc","gnoll","goblin","hobgoblin"]
    ,       randgender                  =   ["male","female"]
	,		randsocialclass				=	["upperclass","middleclass","middleclass","middleclass","middleclass","middleclass","middleclass","middleclass","middleclass","middleclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass","upperclass"]
	,       human                       =   ["Acolyte","Acolyte","Acolyte","Acolyte","Acolyte","Anthropologist","Anthropologist","Anthropologist","Anthropologist","Anthropologist","Archaeologist","Archaeologist","Archaeologist","Archaeologist","Archaeologist","Charlatan","Charlatan","Charlatan","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Entertainer","Entertainer","Faction Agent","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Guild Artisan","Guild Artisan","Hermit","Hermit","Hermit","House Agent","House Agent","House Agent","House Agent","House Agent","Noble","Outlander","Outlander","Outlander","Sage","Sailor","Sailor","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin","Urchin","Urchin","Urchin","Urchin","Urchin"]
	,       halfling                    =   ["Acolyte","Acolyte","Acolyte","Acolyte","Acolyte","Anthropologist","Anthropologist","Anthropologist","Anthropologist","Anthropologist","Archaeologist","Archaeologist","Archaeologist","Archaeologist","Archaeologist","Charlatan","Charlatan","Charlatan","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Entertainer","Entertainer","Faction Agent","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Guild Artisan","Guild Artisan","Hermit","Hermit","Hermit","House Agent","House Agent","House Agent","House Agent","House Agent","Noble","Outlander","Outlander","Outlander","Sage","Sailor","Sailor","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin","Urchin","Urchin","Urchin","Urchin","Urchin"]
    ,       elf                         =   ["Acolyte","Acolyte","Acolyte","Anthropologist","Anthropologist","Anthropologist","Archaeologist","Archaeologist","Archaeologist","Charlatan","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Faction Agent","Folk Hero","Guild Artisan","Guild Artisan","Guild Artisan","Hermit","House Agent","House Agent","House Agent","House Agent","House Agent","Noble","Outlander","Outlander","Outlander","Outlander","Outlander","Sage","Sage","Sage","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin"]
    ,       dwarf                       =   ["Acolyte","Acolyte","Acolyte","Anthropologist","Anthropologist","Anthropologist","Archaeologist","Archaeologist","Archaeologist","Charlatan","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Faction Agent","Folk Hero","Guild Artisan","Guild Artisan","Guild Artisan","Guild Artisan","Guild Artisan","Hermit","House Agent","House Agent","House Agent","House Agent","House Agent","Outlander","Outlander","Outlander","Outlander","Outlander","Sage","Sage","Sage","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin"]
    ,       gnome                       =   ["Acolyte","Acolyte","Acolyte","Anthropologist","Anthropologist","Anthropologist","Anthropologist","Anthropologist","Archaeologist","Archaeologist","Archaeologist","Archaeologist","Archaeologist","Charlatan","Charlatan","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Entertainer","Entertainer","Faction Agent","Folk Hero","Guild Artisan","Guild Artisan","Guild Artisan","Guild Artisan","Guild Artisan","Hermit","House Agent","House Agent","House Agent","House Agent","House Agent","Noble","Outlander","Outlander","Outlander","Sage","Sage","Sage","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin"]
    ,       orc                         =   ["Acolyte","Acolyte","Acolyte","Anthropologist","Archaeologist","Charlatan","Charlatan","Charlatan","Charlatan","Charlatan","Criminal","Criminal","Criminal","Criminal","Criminal","Entertainer","Faction Agent","Faction Agent","Faction Agent","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Hermit","Hermit","Hermit","House Agent","House Agent","House Agent","House Agent","House Agent","Noble","Outlander","Outlander","Outlander","Sage","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin","Urchin","Urchin","Urchin","Urchin","Urchin"]
    ,       warforged                   =   ["Acolyte","Acolyte","Acolyte","Anthropologist","Archaeologist","Charlatan","Criminal","Criminal","Criminal","Entertainer","Faction Agent","Faction Agent","Faction Agent","Folk Hero","Guild Artisan","Guild Artisan","Guild Artisan","Hermit","House Agent","House Agent","House Agent","Noble","Outlander","Sage","Sage","Sage","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin"]
    ,       shifter                     =   ["Acolyte","Anthropologist","Archaeologist","Charlatan","Charlatan","Charlatan","Charlatan","Charlatan","Criminal","Criminal","Criminal","Criminal","Criminal","Entertainer","Faction Hero","Faction Hero","Faction Hero","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Hermit","Hermit","Hermit","Hermit","Hermit","House Agent","House Agent","House Agent","House Agent","House Agent","Noble","Outlander","Outlander","Outlander","Outlander","Outlander","Sage","Sailor","Soldier","Soldier","Soldier","Urchin","Urchin","Urchin","Urchin","Urchin"]
    ,       changling                   =   ["Acolyte","Anthropologist","Archaeologist","Charlatan","Charlatan","Charlatan","Charlatan","Charlatan","Criminal","Criminal","Criminal","Criminal","Criminal","Entertainer","Faction Hero","Faction Hero","Faction Hero","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Hermit","Hermit","Hermit","Hermit","Hermit","House Agent","House Agent","House Agent","House Agent","House Agent","Noble","Outlander","Outlander","Outlander","Outlander","Outlander","Sage","Sailor","Soldier","Soldier","Soldier","Urchin","Urchin","Urchin","Urchin","Urchin"]
    ,       kalashtar                   =   ["Acolyte","Acolyte","Acolyte","Anthropologist","Anthropologist","Anthropologist","Anthropologist","Anthropologist","Anthropologist","Archaeologist","Archaeologist","Archaeologist","Archaeologist","Archaeologist","Charlatan","Charlatan","Charlatan","Charlatan","Charlatan","Criminal","Entertainer","Faction Hero","Folk Hero","Guild Artisan","Hermit","Hermit","Hermit","Hermit","Hermit","House Agent","Noble","Noble","Noble","Outlander","Outlander","Outlander","Outlander","Outlander","Sage","Sage","Sage","Sage","Sage","Sailor","Soldier","Urchin"]
    ,       gnoll                       =   ["Acolyte","Anthropologist","Archaeologist","Charlatan","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Faction Agent","Faction Agent","Faction Agent","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Hermit","Hermit","Hermit","House Agent","Noble","Outlander","Outlander","Outlander","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin","Urchin","Urchin"]
    ,       goblin                      =   ["Acolyte","Anthropologist","Archaeologist","Charlatan","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Faction Agent","Faction Agent","Faction Agent","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Hermit","Hermit","Hermit","House Agent","Noble","Outlander","Outlander","Outlander","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin","Urchin","Urchin"]
    ,       hobgoblin                   =   ["Acolyte","Anthropologist","Archaeologist","Charlatan","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Faction Agent","Faction Agent","Faction Agent","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Hermit","Hermit","Hermit","House Agent","Noble","Outlander","Outlander","Outlander","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin","Urchin","Urchin"]
    ,       upperclass                  =   ["Acolyte","Acolyte","Acolyte","Anthropologist","Anthropologist","Anthropologist","Archaeologist","Archaeologist","Archaeologist","Charlatan","Criminal","Entertainer","Entertainer","Entertainer","Faction Agent","Faction Agent","Faction Agent","Faction Agent","Faction Agent","Folk Hero","Guild Artisan","Guild Artisan","Guild Artisan","Hermit","House Agent","House Agent","House Agent","Noble","Noble","Noble","Outlander","Sage","Sage","Sage","Sailor","Soldier","Soldier","Soldier","Urchin"]
    ,       middleclass                 =   ["Acolyte","Acolyte","Acolyte","Anthropologist","Archaeologist","Charlatan","Charlatan","Charlatan","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Entertainer","Entertainer","Faction Agent","Faction Agent","Faction Agent","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Guild Artisan","Guild Artisan","Hermit","Hermit","Hermit","House Agent","House Agent","House Agent","House Agent","House Agent","Noble","Outlander","Sage","Sage","Sage","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin"]
    ,       lowerclass                  =   ["Acolyte","Anthropologist","Archaeologist","Charlatan","Charlatan","Charlatan","Charlatan","Charlatan","Criminal","Criminal","Criminal","Criminal","Criminal","Entertainer","Entertainer","Entertainer","Entertainer","Entertainer","Faction Agent","Folk Hero","Folk Hero","Folk Hero","Folk Hero","Folk Hero","Guild Artisan","Guild Artisan","Guild Artisan","Hermit","Hermit","Hermit","House Agent","Noble","Outlander","Outlander","Outlander","Sage","Sailor","Sailor","Sailor","Soldier","Soldier","Soldier","Soldier","Soldier","Urchin","Urchin","Urchin","Urchin","Urchin"]
    ,	    acolytepersonality		    =	["I idolize a particular hero of my faith, and constantly refer to that person's deeds and example.","I can find common ground between the fiercest enemies, empathizing with them and always working toward peace.","I see omens in every event and action. The gods try to speak to us, we just need to listen.","Nothing can shake my optimistic attitude.","I quote (or misquote) sacred texts and proverbs in almost every situation.","I am tolerant (or intolerant) of other faiths and respect (or condemn) the worship of other gods.","I've enjoyed fine food, drink, and high society among my temple's elite. Rough living grates on me.","I've spent so long in the temple that I have little practical experience dealing with people in the outside world."]
    ,	    acolyteideal			    =	["Tradition. The ancient traditions of worship and sacrifice must be preserved and upheld. (Lawful)","Charity. I always try to help those in need, no matter what the personal cost. (Good)","Change. We must help bring about the changes the gods are constantly working in the world. (Chaotic)","Power. I hope to one day rise to the top of my faith's religious hierarchy. (Lawful)","Faith. I trust that my deity will guide my actions. I have faith that if I work hard, things will go well. (Lawful)","Aspiration. I seek to prove myself worthy of my god's favor by matching my actions against his or her teachings. (Any)"]
    ,	    acolytebond				    =	["I would die to recover an ancient relic of my faith that was lost long ago.","I will someday get revenge on the corrupt temple hierarchy who branded me a heretic.","I owe my life to the priest who took me in when my parents died.","Everything I do is for the common people.","I will do anything to protect the temple where I served.","I seek to preserve a sacred text that my enemies consider heretical and seek to destroy."]
    ,	    acolyteflaw				    =	["I judge others harshly, and myself even more severely.","I put too much trust in those who wield power within my temple's hierarchy.","My piety sometimes leads me to blindly trust those that profess faith in my god.","I am inflexible in my thinking.","I am suspicious of strangers and expect the worst of them.","Once I pick a goal, I become obsessed with it to the detriment of everything else in my life."]
    ,	    anthropologistpersonality	=	["I prefer the company of those who aren't like me, including people of other races","I'm a stickler when it comes to observing proper etiquette and local customs","I would rather observe than meddle","By living among violent people, I have become desensitized to violence.","I would risk life and limb to discover a new culture or unravel the secrets of a dead one.","When I arrive at a new settlement for the first time, I must learn all its customs."]
    ,	    anthropologyideal			=	["Discovery. I want to be the first person to discover a lost culture. (Any)","Distance. One must not interfere with the affairs of another culture - even one in need of aid. (Lawful)","Knowledge. By understanding other races and cultures, we learn to understand ourselves. (Any)","Power. Common people crave strong leadership, and I do my utmost to provide it. (Lawful)","Protection. I must do everything possible to save a society facing extinction. (Good)","Indifferent. Life is cruel. What's the point in saving people if they're going to die anyway? (Chaotic)"]
    ,	    anthropologybond			=	["My mentor gave me a journal filled with lore and wisdom. Losing it would devastate me.","Having lived among the people of a primeval tribe or clan, I long to return and see how they are faring.","Years ago, tragedy struck the members of an isolated society I befriended, and I will honor them.","I want to learn more about a particular humanoid culture that fascinates me.","I seek to avenge a clan, tribe, kingdom, or empire that was wiped out.","I have a trinket that I believe is the key to finding a long-lost society."]
    ,	    anthropologyflaw			=	["Boats make me seasick.","I talk to myself, and I don't make friends easily.","I believe that I'm intellectually superior to people from other cultures and have much to teach them.","I've picked up some unpleasant habits living among goblins, lizardfolk, or orcs.","I complain about everything.","I wear a tribal mask and never take it off."]
	,		archaeologistpersonality	=	["I love a good puzzle or mystery","I'm a pack rat who never throws anything away.","Fame is more important to me than money.","I have no qualms about stealing from the dead.","I'm happier in a dusty old tomb than I am in the centers of civilization.","Traps don't make me nervous. Idiots who trigger traps make me nervous.","I might fail, but I will never give up.","You might think I'm a scholar, but I love a good brawl. These fists were made for punching."]
	,		archaeologistideal			=	["Preservation. That artifact belongs in a museum. (Good)","Greed. I won't risk my life for nothing. I expect some kind of payment. (Any)","Death Wish. Nothing is more exhilarating than a narrow escape from the jaws of death. (Chaotic)","Dignity. The dead and their belongings deserve to be treated with respect. (Lawful)","Immortality. All of my exploring is part of a plan to find the secret of everlasting life. (Any)","Danger. With every great discovery comes grave danger. The two walk hand in hand. (Any)"]
	,		archaeologistbond			=	["Ever since I was a child, I've heard stories about a lost city. I aim to find it, learn its secrets, and earn my place in the history books.","I want to find my mentor, who disappeared on an expedition some time ago.","I have a friendly rival. Only one of us can be the best, and I aim to prove it's me.","I won't sell an art object or other treasure that has historical significance or is one of a kind.","I'm secretly in love with the wealthy patron who sponsors my archaeological exploits.","I hope to bring prestige to a library, a museum, or a university."]
	,		archaeologistflaw			=	["I have a secret fear of some common wild animal - and in my work, I see them everywhere.","I can't leave a room without searching it for secret doors.","When I'm not exploring dungeons or ruins. I get jittery and impatient.","I have no time for friends or family. I spend every waking moment thinking about and preparing for my next expedition.","When given the choice of going left or right, I always go left.","I can't sleep except in total darkness."]
	,		charlatanpersonality		=	["I fall in and out of love easily, and am always pursuing someone.","I have a joke for every occasion, especially occasions where humor is inappropriate.","Flattery is my preferred trick for getting what I want.","I'm a born gambler who can't resist taking a risk for a potential payoff.","I lie about almost everything, even when there's no reason to.","Sarcasm and insults are my weapons of choice.","I keep multiple holy symbols on me and invoke whatever deity might come in useful at any given moment.","I pocket anything I see that might have some value."]
	,		charlatanideal				=	["Independence. I am a free spirit—no one tells me what to do. (Chaotic)","Fairness. I never target people who can't afford to lose a few coins. (Lawful)","Charity. I distribute the money I acquire to the people who really need it. (Good)","Creativity. I never run the same con twice. (Chaotic)","Friendship. Material goods come and go. Bonds of friendship last forever. (Good)","Aspiration. I'm determined to make something of myself. (Any)"]
	,		charlatanbond				=	["I fleeced the wrong person and must work to ensure that this individual never crosses paths with me or those I care about.","I owe everything to my mentor—a horrible person who's probably rotting in jail somewhere.","Somewhere out there, I have a child who doesn't know me. I'm making the world better for him or her.","I come from a noble family, and one day I'll reclaim my lands and title from those who stole them from me.","A powerful person killed someone I love. Some day soon, I'll have my revenge.","I swindled and ruined a person who didn't deserve it. I seek to atone for my misdeeds but might never be able to forgive myself."]
	,		charlatanflaw				=	["I can't resist a pretty face.","I'm always in debt. I spend my ill-gotten gains on decadent luxuries faster than I bring them in.","I'm convinced that no one could ever fool me the way I fool others.","I'm too greedy for my own good. I can't resist taking a risk if there's money involved.","I can't resist swindling people who are more powerful than me.","I hate to admit it and will hate myself for it, but I'll run and preserve my own hide if the going gets tough."]
	,		criminalpersonality			=	["I always have a plan for when things go wrong.","I am always calm, no matter what the situation. I never raise my voice or let my emotions control me.","The first thing I do in a new place is note the locations of everything valuable—or where such things could be hidden.","I would rather make a new friend than a new enemy.","I am incredibly slow to trust. Those who seem the fairest often have the most to hide.","I don't pay attention to the risks in a situation. Never tell me the odds.","The best way to get me to do something is to tell me I can't do it.","I blow up at the slightest insult."]
	,		criminalideal				=	["Honor. I don't steal from others in the trade. (Lawful)","Freedom. Chains are meant to be broken, as are those who would forge them. (Chaotic)","Charity. I steal from the wealthy so that I can help people in need. (Good)","Greed. I will do whatever it takes to become wealthy. (Evil)","People. I'm loyal to my friends, not to any ideals, and everyone else can take a trip down the Styx for all I care. (Neutral)","Redemption. There's a spark of good in everyone. (Good)"]
	,		criminalbond				=	["I'm trying to pay off an old debt I owe to a generous benefactor.","My ill-gotten gains go to support my family.","Something important was taken from me, and I aim to steal it back.","I will become the greatest thief that ever lived.","I'm guilty of a terrible crime. I hope I can redeem myself for it.","Someone I loved died because of a mistake I made. That will never happen again."]
	,		criminalflaw				=	["When I see something valuable, I can't think about anything but how to steal it.","When faced with a choice between money and my friends, I usually choose the money.","If there's a plan, I'll forget it. If I don't forget it, I'll ignore it.","I have a 'tell' that reveals when I'm lying.","I turn tail and run when things look bad.","An innocent person is in prison for a crime that I committed. I'm okay with that."]
	,		entertainerpersonality		=	["I know a story relevant to almost every situation.","Whenever I come to a new place, I collect local rumors and spread gossip.","I'm a hopeless romantic, always searching for that 'special someone'.","Nobody stays angry at me or around me for long, since I can defuse any amount of tension.","I love a good insult, even one directed at me.","I get bitter if I'm not the center of attention.","I'll settle for nothing less than perfection.","I change my mood or my mind as quickly as I change key in a song."]
	,		entertainerideal			=	["Beauty. When I perform, I make the world better than it was. (Good)","Tradition. The stories, legends, and songs of the past must never be forgotten, for they teach us who we are. (Lawful)","Creativity. The world is in need of new ideas and bold action. (Chaotic)","Greed. I'm only in it for the money and fame. (Evil)","People. I like seeing the smiles on people's faces when I perform. That's all that matters. (Neutral)","Honesty. Art should reflect the soul; it should come from within and reveal who we really are. (Any)"]
	,		entertainerbond				=	["My instrument is my most treasured possession, and it reminds me of someone I love.","Someone stole my precious instrument, and someday I'll get it back.","I want to be famous, whatever it takes.","I idolize a hero of the old tales and measure my deeds against that person's.","I will do anything to prove myself superior to my hated rival.","I would do anything for the other members of my old troupe."]
	,		entertainerflaw				=	["I'll do anything to win fame and renown.","I'm a sucker for a pretty face.","A scandal prevents me from ever going home again. That kind of trouble seems to follow me around.","I once satirized a noble who still wants my head. It was a mistake that I will likely repeat.","I have trouble keeping my true feelings hidden. My sharp tongue lands me in trouble.","Despite my best efforts, I am unreliable to my friends."]
	,		folkheropersonality			=	["I judge people by their actions, not their words.","If someone is in trouble, I'm always ready to lend help.","When I set my mind to something, I follow through no matter what gets in my way.","I have a strong sense of fair play and always try to find the most equitable solution to arguments.","I'm confident in my own abilities and do what I can to instill confidence in others.","Thinking is for other people. I prefer action.","I misuse long words in an attempt to sound smarter.","I get bored easily. When am I going to get on with my destiny?"]
	,		folkheroideal				=	["Respect. People deserve to be treated with dignity and respect. (Good)","Fairness. No one should get preferential treatment before the law, and no one is above the law. (Lawful)","Freedom. Tyrants must not be allowed to oppress the people. (Chaotic)","Might. If I become strong, I can take what I want—what I deserve. (Evil)","Sincerity. There's no good in pretending to be something I'm not. (Neutral)","Destiny. Nothing and no one can steer me away from my higher calling. (Any)"]
	,		folkherobond				=	["I have a family, but I have no idea where they are. One day, I hope to see them again.","I worked the land, I love the land, and I will protect the land.","A proud noble once gave me a horrible beating, and I will take my revenge on any bully I encounter.","My tools are symbols of my past life, and I carry them so that I will never forget my roots.","I protect those who cannot protect themselves.","I wish my childhood sweetheart had come with me to pursue my destiny."]
	,		folkheroflaw				=	["The tyrant who rules my land will stop at nothing to see me killed.","I'm convinced of the significance of my destiny, and blind to my shortcomings and the risk of failure.","The people who knew me when I was young know my shameful secret, so I can never go home again.","I have a weakness for the vices of the city, especially hard drink.","Secretly, I believe that things would be better if I were a tyrant lording over the land.","I have trouble trusting in my allies."]
	,		guildartisanpersonality		=	["I believe that anything worth doing is worth doing right. I can't help it—I'm a perfectionist.","I'm a snob who looks down on those who can't appreciate fine art.","I always want to know how things work and what makes people tick.","I'm full of witty aphorisms and have a proverb for every occasion.","I'm rude to people who lack my commitment to hard work and fair play.","I like to talk at length about my profession.","I don't part with my money easily and will haggle tirelessly to get the best deal possible.","I'm well known for my work, and I want to make sure everyone appreciates it. I'm always taken aback when people haven't heard of me."]
	,		guildartisanideal			=	["Community. It is the duty of all civilized people to strengthen the bonds of community and the security of civilization. (Lawful)","Generosity. My talents were given to me so that I could use them to benefit the world. (Good)","Freedom. Everyone should be free to pursue his or her own livelihood. (Chaotic)","Greed. I'm only in it for the money. (Evil)","People. I'm committed to the people I care about, not to ideals. (Neutral)","Aspiration. I work hard to be the best there is at my craft. (Any)"]
	,		guildartisanbond			=	["The workshop where I learned my trade is the most important place in the world to me.","I created a great work for someone, and then found them unworthy to receive it. I'm still looking for someone worthy.","I owe my guild a great debt for forging me into the person I am today.","I pursue wealth to secure someone's love.","One day I will return to my guild and prove that I am the greatest artisan of them all.","I will get revenge on the evil forces that destroyed my place of business and ruined my livelihood."]
	,		guildartisanflaw			=	["I'll do anything to get my hands on something rare or priceless.","I'm quick to assume that someone is trying to cheat me.","No one must ever learn that I once stole money from guild coffers.","I'm never satisfied with what I have—I always want more.","I would kill to acquire a noble title.","I'm horribly jealous of anyone who can outshine my handiwork. Everywhere I go, I'm surrounded by rivals."]
	,		hermitpersonality			=	["I've been isolated for so long that I rarely speak, preferring gestures and the occasional grunt.","I am utterly serene, even in the face of disaster.","The leader of my community had something wise to say on every topic, and I am eager to share that wisdom.","I feel tremendous empathy for all who suffer.","I'm oblivious to etiquette and social expectations.","I connect everything that happens to me to a grand, cosmic plan.","I often get lost in my own thoughts and contemplation, becoming oblivious to my surroundings.","I am working on a grand philosophical theory and love sharing my ideas."]
	,		hermitideal					=	["Greater Good. My gifts are meant to be shared with all, not used for my own benefit. (Good)","Logic. Emotions must not cloud our sense of what is right and true, or our logical thinking. (Lawful)","Free Thinking. Inquiry and curiosity are the pillars of progress. (Chaotic)","Power. Solitude and contemplation are paths toward mystical or magical power. (Evil)","Live and Let Live. Meddling in the affairs of others only causes trouble. (Neutral)","Self-Knowledge. If you know yourself, there's nothing left to know. (Any)"]
	,		hermitbond					=	["Nothing is more important than the other members of my hermitage, order, or association.","I entered seclusion to hide from the ones who might still be hunting me. I must someday confront them.","I'm still seeking the enlightenment I pursued in my seclusion, and it still eludes me.","I entered seclusion because I loved someone I could not have.","Should my discovery come to light, it could bring ruin to the world.","My isolation gave me great insight into a great evil that only I can destroy."]
	,		hermitflaw					=	["Now that I've returned to the world, I enjoy its delights a little too much.","I harbor dark, bloodthirsty thoughts that my isolation and meditation failed to quell.","I am dogmatic in my thoughts and philosophy.","I let my need to win arguments overshadow friendships and harmony.","I'd risk too much to uncover a lost bit of knowledge.","I like keeping secrets and won't share them with anyone."]
	,		noblepersonality			=	["My eloquent flattery makes everyone I talk to feel like the most wonderful and important person in the world.","The common folk love me for my kindness and generosity.","No one could doubt by looking at my regal bearing that I am a cut above the unwashed masses.","I take great pains to always look my best and follow the latest fashions.","I don't like to get my hands dirty, and I won't be caught dead in unsuitable accommodations.","Despite my noble birth, I do not place myself above other folk. We all have the same blood.","My favor, once lost, is lost forever.","If you do me an injury, I will crush you, ruin your name, and salt your fields."]
	,		nobleideal					=	["Respect. Respect is due to me because of my position, but all people regardless of station deserve to be treated with dignity. (Good)","Responsibility. It is my duty to respect the authority of those above me, just as those below me must respect mine. (Lawful)","Independence. I must prove that I can handle myself without coddling from my family. (Chaotic)","Power. If I can attain more power, no one will tell me what to do. (Evil)","Family. Blood runs thicker than water. (Any)","Noble Obligation. It is my duty to protect and care for the people beneath me. (Good)"]
	,		noblebond					=	["I will face any challenge to win the approval of my family.","My house's alliance with another noble family must be sustained at all costs.","Nothing is more important than the other members of my family.","I am in love with the heir of a family that my family despises.","My loyalty to my sovereign is unwavering.","The common folk must see me as a hero of the people."]
	,		nobleflaw					=	["I secretly believe that everyone is beneath me.","I hide a truly scandalous secret that could ruin my family forever.","I too often hear veiled insults and threats in every word addressed to me, and I'm quick to anger.","I have an insatiable desire for carnal pleasures.","In fact, the world does revolve around me.","By my words and actions, I often bring shame to my family."]
	,		outlanderpersonality		=	["I'm driven by a wanderlust that led me away from home","I watch over my friends as if they were a litter of newborn pups.","I once ran twenty-five miles without stopping to warn to my clan of an approaching orc horde. I'd do it again if I had to.","I have a lesson for every situation, drawn from observing nature.","I place no stock in wealthy or well-mannered folk. Money and manners won't save you from a hungry owlbear.","I'm always picking things up, absently fiddling with them, and sometimes accidentally breaking them.","I feel far more comfortable around animals than people","I was, in fact, raised by wolves."]
	,		outlanderideal				=	["Change. Life is like the seasons, in constant change, and we must change with it. (Chaotic)","Greater Good. It is each person's responsibility to make the most happiness for the whole tribe. (Good)","Honor. If I dishonor myself, I dishonor my whole clan. (Lawful)","Might. The strongest are meant to rule. (Evil)","Nature. The natural world is more important than all the constructs of civilization. (Neutral)","Glory. I must earn glory in battle, for myself and my clan. (Any)"]
	,		outlanderbond				=	["My family, clan, or tribe is the most important thing in my life, even when they are far from me.","An injury to the unspoiled wilderness of my home is an injury to me.","I will bring terrible wrath down on the evildoers who destroyed my homeland.","I am the last of my tribe, and it is up to me to ensure their names enter legend.","I suffer awful visions of a coming disaster and will do anything to prevent it.","It is my duty to provide children to sustain my tribe."]
	,		outlanderflaw				=	["I am too enamored of ale, wine, and other intoxicants.","There's no room for caution in a life lived to the fullest.","I remember every insult I've received and nurse a silent resentment toward anyone who's ever wronged me.","I am slow to trust members of other races, tribes, and societies.","Violence is my answer to almost any challenge.","Don't expect me to save those who can't save themselves. It is nature's way that the strong thrive and the weak perish."]
	,		sagepersonality				=	["I use polysyllabic words that convey the impression of great erudition.","I've read every book in the world's greatest libraries—or I like to boast that I have.","I'm used to helping out those who aren't as smart as I am, and I patiently explain anything and everything to others.","There's nothing I like more than a good mystery.","I'm willing to listen to every side of an argument before I make my own judgment.","I . . . speak . . . slowly . . . when talking . . . to idiots, . . . which . . . almost . . . everyone . . . is . . . compared . . . to me.","I am horribly, horribly awkward in social situations.","I'm convinced that people are always trying to steal my secrets."]
	,		sageideal					=	["Knowledge. The path to power and self-improvement is through knowledge. (Neutral)","Beauty. What is beautiful points us beyond itself toward what is true. (Good)","Logic. Emotions must not cloud our logical thinking. (Lawful)","No Limits. Nothing should fetter the infinite possibility inherent in all existence. (Chaotic)","Power. Knowledge is the path to power and domination. (Evil)","Self-Improvement. The goal of a life of study is the betterment of oneself. (Any)"]
	,		sagebond					=	["It is my duty to protect my students.","I have an ancient text that holds terrible secrets that must not fall into the wrong hands.","I work to preserve a library, university, scriptorium, or monastery.","My life's work is a series of tomes related to a specific field of lore.","I've been searching my whole life for the answer to a certain question.","I sold my soul for knowledge. I hope to do great deeds and win it back."]
	,		sageflaw					=	["I am easily distracted by the promise of information.","Most people scream and run when they see a demon. I stop and take notes on its anatomy.","Unlocking an ancient mystery is worth the price of a civilization.","I overlook obvious solutions in favor of complicated ones.","I speak without really thinking through my words, invariably insulting others.","I can't keep a secret to save my life, or anyone else's."]
	,		sailorpersonality			=	["My friends know they can rely on me, no matter what.","I work hard so that I can play hard when the work is done.","I enjoy sailing into new ports and making new friends over a flagon of ale.","I stretch the truth for the sake of a good story.","To me, a tavern brawl is a nice way to get to know a new city.","I never pass up a friendly wager.","My language is as foul as an otyugh nest.","I like a job well done, especially if I can convince someone else to do it."]
	,		sailorideal					=	["Respect. The thing that keeps a ship together is mutual respect between captain and crew. (Good)","Fairness. We all do the work, so we all share in the rewards. (Lawful)","Freedom. The sea is freedom—the freedom to go anywhere and do anything. (Chaotic)","Mastery. I'm a predator, and the other ships on the sea are my prey. (Evil)","People. I'm committed to my crewmates, not to ideals. (Neutral)","Aspiration. Someday, I'll own my own ship and chart my own destiny. (Any)"]
	,		sailorbond					=	["I'm loyal to my captain first, everything else second.","The ship is most important—crewmates and captains come and go.","I'll always remember my first ship.","In a harbor town, I have a paramour whose eyes nearly stole me from the sea.","I was cheated out of my fair share of the profits, and I want to get my due.","Ruthless pirates murdered my captain and crewmates, plundered our ship, and left me to die. Vengeance will be mine."]
	,		sailorflaw					=	["I follow orders, even if I think they're wrong.","I'll say anything to avoid having to do extra work.","Once someone questions my courage, I never back down no matter how dangerous the situation.","Once I start drinking, it's hard for me to stop.","I can't help but pocket loose coins and other trinkets I come across.","My pride will probably lead to my destruction."]
	,		soldierpersonality			=	["I'm always polite and respectful.","I'm haunted by memories of war. I can't get the images of violence out of my mind.","I've lost too many friends, and I'm slow to make new ones.","I'm full of inspiring and cautionary tales from my military experience relevant to almost every combat situation.","I can stare down a hell hound without flinching.","I enjoy being strong and like breaking things.","I have a crude sense of humor.","I face problems head-on. A simple, direct solution is the best path to success."]
	,		soldierideal				=	["Greater Good. Our lot is to lay down our lives in defense of others. (Good)","Responsibility. I do what I must and obey just authority. (Lawful)","Independence. When people follow orders blindly, they embrace a kind of tyranny. (Chaotic)","Might. In life as in war, the stronger force wins. (Evil)","Live and Let Live. Ideals aren't worth killing over or going to war for. (Neutral)","Nation. My city, nation, or people are all that matter. (Any)"]
	,		soldierbond					=	["I would still lay down my life for the people I served with.","Someone saved my life on the battlefield. To this day, I will never leave a friend behind.","My honor is my life.","I'll never forget the crushing defeat my company suffered or the enemies who dealt it.","Those who fight beside me are those worth dying for.","I fight for those who cannot fight for themselves."]
	,		soldierflaw					=	["The monstrous enemy we faced in battle still leaves me quivering with fear.","I have little respect for anyone who is not a proven warrior.","I made a terrible mistake in battle that cost many lives—and I would do anything to keep that mistake secret.","My hatred of my enemies is blinding and unreasoning.","I obey the law, even if the law causes misery.","I'd rather eat my armor than admit when I'm wrong."]
	,		urchinpersonality			=	["I hide scraps of food and trinkets away in my pockets.","I ask a lot of questions.","I like to squeeze into small places where no one else can get to me.","I sleep with my back to a wall or tree, with everything I own wrapped in a bundle in my arms.","I eat like a pig and have bad manners.","I think anyone who's nice to me is hiding evil intent.","I don't like to bathe.","I bluntly say what others are hinting at or hiding."]
	,		urchinideal					=	["Respect. All people, rich or poor, deserve respect. (Good)","Community. We have to take care of each other, because no one else is going to do it. (Lawful)","Change. The low are lifted up, and the high and mighty are brought down. Change is the nature of things. (Chaotic)","Retribution. The rich need to be shown what life and death are like in the gutters. (Evil)","People. I help the people who help me—that's what keeps us alive. (Neutral)","Aspiration. I'm going to prove that I'm worthy of a better life. (Any)"]
	,		urchinbond					=	["My town is my city or my home, and I'll fight to defend it.","I sponsor an orphanage to keep others from enduring what I was forced to endure.","I owe my survival to another urchin who taught me to live on the streets.","I owe a debt I can never repay to the person who took pity on me.","I escaped my life of poverty by robbing an important person, and I'm wanted for it.","No one else should have to endure the hardships I've been through."]
	,		urchinflaw					=	["If I'm outnumbered, I will run away from a fight.","Gold seems like a lot of money to me, and I'll do just about anything for more of it.","I will never fully trust anyone other than myself.","I'd rather kill someone in their sleep than fight fair.","It's not stealing if I need it more than someone else.","People who can't take care of themselves get what they deserve."]
    if (msg.type == "api" && msg.content.indexOf("!tst") !== -1) {
        let cmds = msg.content.split(/\s+/);
		if (cmds[1] === "random")
			{
				cmds[1] = _.sample(randrace)
			}
		if (cmds[2] === "random")
			{
				cmds[2] = _.sample(randgender)
			}
		if (cmds[3] === "random")
			{
				cmds[3] = _.sample(randsocialclass)
			} 
        if (cmds[1] === "aundairan")
            {
                var race = "Aundarian human"
                ,   heightroll = randomInteger(9)
                ,   height = Math.floor((65 + heightroll) / 12) + " Feet " + ((65 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 120 + " lbs"
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([human.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([human.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([human.concat(lowerclass)])
					}
				if (cmds[2] === "male")
                    {
                        var gender = "male"
                        ,   name = aundarianmalefirst + " " + aundarianlast
                    }
                if (cmds[2] === "female")
                    {
                           var gender = "female"
                       ,   name = aundarianfemalefirst + " " + aundarianlast
                    }
            }
        if (cmds[1] === "brelish")
            {
                var race = "Brelish human"
                ,   heightroll = randomInteger(9)
                ,   height = Math.floor((65 + heightroll) / 12) + " Feet " + ((65 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 120 + " lbs"
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([human.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([human.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([human.concat(lowerclass)])
					}
                if (cmds[2] === "male")
                    {
                        var gender = "male"
                         ,   name = brelishmalefirst + " " + brelishlast
                    }
                if (cmds[2] === "female")
                    {
                        var gender = "female"
                        ,   name = brelishfemalefirst + " " + brelishlast
                    }    
            }
        if (cmds[1] === "karrnathi")
            {
                var race = "Karrnathi human"
                ,   heightroll = randomInteger(9)
                ,   height = Math.floor((65 + heightroll) / 12) + " Feet " + ((65 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 120 + " lbs"
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([human.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([human.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([human.concat(lowerclass)])
					}
                if (cmds[2] === "male")
                    {
                        var gender = "male"
                        ,   name = karrnathimalefirst + " " + karrnathilast
                    }
                if (cmds[2] === "female")
                    {
                        var gender = "female"
                        ,   name = karrnathifemalefirst + " " + karrnathilast
                    }
            }
        if (cmds[1] === "thrane")
            {
                var race = "Thrane human"
                ,   heightroll = randomInteger(9)
                ,   height = Math.floor((65 + heightroll) / 12) + " Feet " + ((65 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 120 + " lbs"
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([human.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([human.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([human.concat(lowerclass)])
					}
                if (cmds[2] === "male")
                    {
                        var gender = "male"
                        ,   name = thranemalefirst + " " + thranelast
                    }
                if (cmds[2] === "female")
                    {
                        var gender = "female"
                        ,   name = thranefemalefirst + " " + thranelast
                    }
            }
      if (cmds[1] === "dwarf")
            {
                var race = "Dwarf"
                ,   heightroll = randomInteger(9)
                ,   height = Math.floor((50 + heightroll) / 12) + " Feet " + ((50 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 160 + " lbs"
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([dwarf.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([dwarf.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([dwarf.concat(lowerclass)])
					}
                if (cmds[2] === "male")
                    {
                        var gender = "male"
                        ,   name = dwarfmalefirst + " " + dwarfclanname
                    }            
                if (cmds[2] === "female")
                    {
                        var gender = "female"
                        ,   name = dwarffemalefirst + " " + dwarfclanname
                    }
            }
        if (cmds[1] === "elf")
            {
                var name = elffirstname + " " + elflastname
                ,   race = "Elf"
                ,   heightroll = randomInteger(9)
                ,   height = Math.floor((63 + heightroll) / 12) + " Feet " + ((63 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 120 + " lbs"
                ,   gender = cmds[2]
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([elf.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([elf.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([elf.concat(lowerclass)])
					}
            }
        if (cmds[1] === "gnome")
            {
                var race = "Gnome"
                ,   heightroll = randomInteger(9)
                ,   height = Math.floor((65 + heightroll) / 12) + " Feet " + ((65 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 120 + " lbs"
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([gnome.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([gnome.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([gnome.concat(lowerclass)])
					}
                if (cmds[2] === "male")
                    {
                        var gender = "male"
                        ,   name = gnomemalefirst + " " + gnomelast
                    }
                if (cmds[2] === "female")
                    {
                        var gender = "female"
                        ,   name =  gnomefemalefirst + " " + gnomelast
                    }
            }
        if (cmds[1] === "halfling")
            {
                var race = "Halfing"
                ,   heightroll = randomInteger(5)
                ,   height = Math.floor((45 + heightroll) / 12) + " Feet " + ((45 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll + 75 + randomInteger(6)-1+" lbs"
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([halfling.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([halfling.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([halfling.concat(lowerclass)])
					}
                if (cmds[2] === "male")
                    {
                        var gender = "male"
                        ,   name =  halflingmalefirst + " " + halflinglast
                    }        
                if (cmds[2] === "female")
                    {
                        var gender = "female"
                        ,   name =  halflingfemalefirst + " " + halflinglast
                    }
            }    
        if (cmds[1] === "orc")
            {
                var race = "Orc"
                ,   heightroll = randomInteger(6)
                ,   height = Math.floor((71 + heightroll) / 12) + " Feet " + ((71 + heightroll) % 12) + " Inches Tall"
                ,   weight = (heightroll*5) + randomInteger(5)  + 195 + " lbs"
                ,   gender = "male"
                ,   name = orcfirst + " " + orclast
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([orc.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([orc.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([orc.concat(lowerclass)])
					}
            }
        if (cmds[1] === "gnoll")
            var race = "Gnoll"
            ,   heightroll = randomInteger(9)
            ,   height = Math.floor((65 + heightroll) / 12) + " Feet " + ((65 + heightroll) % 12) + " Inches Tall"
            ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 120 + " lbs"
            ,   gender = cmds[2]
            ,   name = gnollfirst
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([gnoll.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([gnoll.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([gnoll.concat(lowerclass)])
					}
        if (cmds[1] === "goblin")
            var race = "Goblin"
            ,   heightroll = randomInteger(5)
            ,   height = Math.floor((45 + heightroll) / 12) + " Feet " + ((45 + heightroll) % 12) + " Inches Tall"
            ,   weight = heightroll + 75 + randomInteger(6)-1+" lbs"
            ,   gender = cmds[2]
            ,   name = goblinfirst
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([goblin.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([goblin.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([goblin.concat(lowerclass)])
					}
        if (cmds[1] === "hobgoblin")
            var race = "Hobgoblin"
            ,   heightroll = randomInteger(5)
            ,   height = Math.floor((50 + heightroll) / 12) + " Feet " + ((45 + heightroll) % 12) + " Inches Tall"
            ,   weight = heightroll + 95 + randomInteger(6)-1+" lbs"
            ,   gender = cmds[2]
            ,   name = hobgoblinfirst
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([hobgoblin.concat(upperclass)])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([hobgoblin.concat(middleclass)])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([hobgoblin.concat(lowerclass)])
					}
        if (cmds[1] === "warforged")
            var race = "Warforged"
            ,   heightroll = randomInteger(6)
            ,   height = Math.floor((71 + heightroll) / 12) + " Feet " + ((71 + heightroll) % 12) + " Inches Tall"
            ,   weight = (heightroll*5) + randomInteger(5)  + 195 + " lbs"
            ,   gender = cmds[2]
            ,   name = warforgedfirst 
                if (cmds[3] === "upperclass")
					{
						var background = warforged.concat(upperclass)
					}
                if (cmds[3] === "middleclass")
					{
						var background = warforged.concat(middleclass)
					}
                if (cmds[3] === "lowerclass")
					{
						var background = warforged.concat(lowerclass)
					}
			//var background =_.sample(background)
        if (cmds[1] === "halfelf")
            {
                var race = "Halfelf"
                ,   heightroll = randomInteger(9)
                ,   height = Math.floor((65 + heightroll) / 12) + " Feet " + ((65 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 120 + " lbs"
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([elf.concat(human.concat(upperclass))])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([elf.concat(human.concat(middleclass))])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([elf.concat(human.concat(lowerclass))])
					}
                if (cmds[2] === "male")
                    {
                        var gender = "male"
                        ,   name = halfelfmalefirst + " " + halfelflast
                    }
                if (cmds[2] === "female")
                    {
                        var gender = "female"
                        ,   name = halfelffemalefirst + " " + halfelflast
                    }
            }
        if (cmds[1] === "halforc")
            {
                var race = "Halforc"
                ,   heightroll = randomInteger(9)
                ,   height = Math.floor((65 + heightroll) / 12) + " Feet " + ((65 + heightroll) % 12) + " Inches Tall"
                ,   weight = heightroll * (randomInteger(10) - 1) + randomInteger(10) + 120 + " lbs"
                if (cmds[3] === "upperclass")
					{
						var background = _.sample([orc.concat(human.concat(upperclass))])
					}
                if (cmds[3] === "middleclass")
					{
						var background = _.sample([orc.concat(human.concat(middleclass))])
					}
                if (cmds[3] === "lowerclass")
					{
						var background = _.sample([orc.concat(human.concat(lowerclass))])
					}
                if (cmds[2] === "male")
                    {
                        var gender = "male"
                        ,   name = halforcmalefirst + " " + halforclast
                    }
                if (cmds[2] === "female")
                    {
                        var gender = "female"
                        ,   name = halforcfemalefirst + " " + halforclast
                    }
            }
            //sendChat(msg.who,background)
            var backgroundold = background
            var background =_.sample(background)
       		if	(background === "Acolyte")
			{
				var personalitytrait = _.sample(acolytepersonality,2)
				, ideal = _.sample(acolyteideal)
				, bond = _.sample(acolytebond)
				, flaw = _.sample(acolyteflaw)
			}
			else if	(background === "Anthropologist")
			{
				var personalitytrait = _.sample(anthropologistpersonality,2)
				, ideal = _.sample(anthropologistideal)
				, bond = _.sample(anthropologistbond)
				, flaw = _.sample(anthropologistflaw)
			}
			else if	(background === "Archaeologist")
			{
				var personalitytrait = _.sample(archaeologistpersonality,2)
				, ideal = _.sample(archaeologistideal)
				, bond = _.sample(archaeologistbond)
				, flaw = _.sample(archaeologistflaw)
			}
			else if	(background === "Charlatan")
			{
				var personalitytrait = _.sample(charlatanpersonality,2)
				, ideal = _.sample(charlatanideal)
				, bond = _.sample(charlatanbond)
				, flaw = _.sample(charlatanflaw)
			}
			else if	(background === "Criminal")
			{
				var personalitytrait = _.sample(criminalpersonality,2)
				, ideal = _.sample(criminalideal)
				, bond = _.sample(criminalbond)
				, flaw = _.sample(criminalflaw)
			}
			else if	(background === "Entertainer")
			{
				var personalitytrait = _.sample(entertainerpersonality,2)
				, ideal = _.sample(entertainerideal)
				, bond = _.sample(entertainerbond)
				, flaw = _.sample(entertainerflaw)
			}
			else if	(background === "Folk Hero")
			{
				var personalitytrait = _.sample(folkheropersonality,2)
				, ideal = _.sample(folkheroideal)
				, bond = _.sample(folkherobond)
				, flaw = _.sample(folkheroflaw)
			}
			else if	(background === "Guild Artisan")
			{
				var personalitytrait = _.sample(guildartisanpersonality,2)
				, ideal = _.sample(guildartisanideal)
				, bond = _.sample(guildartisanbond)
				, flaw = _.sample(guildartisanflaw)
			}
			else if	(background === "Hermit")
			{
				var personalitytrait = _.sample(hermitpersonality,2)
				, ideal = _.sample(hermitideal)
				, bond = _.sample(hermitbond)
				, flaw = _.sample(hermitflaw)
			}
			else if	(background === "Noble")
			{
				var personalitytrait = _.sample(noblepersonality,2)
				, ideal = _.sample(nobleideal)
				, bond = _.sample(noblebond)
				, flaw = _.sample(nobleflaw)
			}
			else if	(background === "Outlander")
			{
				var personalitytrait = _.sample(outlanderpersonality,2)
				, ideal = _.sample(outlanderideal)
				, bond = _.sample(outlanderbond)
				, flaw = _.sample(outlanderflaw)
			}
			else if	(background === "Sage")
			{
				var personalitytrait = _.sample(sagepersonality,2)
				, ideal = _.sample(sageideal)
				, bond = _.sample(sagebond)
				, flaw = _.sample(sageflaw)
			}
			else if	(background === "Sailor")
			{
				var personalitytrait = _.sample(sailorpersonality,2)
				, ideal = _.sample(sailorideal)
				, bond = _.sample(sailorbond)
				, flaw = _.sample(sailorflaw)
			}
			else if	(background === "Soldier")
			{
				var personalitytrait = _.sample(soldierpersonality,2)
				, ideal = _.sample(soldierideal)
				, bond = _.sample(soldierbond)
				, flaw = _.sample(soldierflaw)
			}
			else if	(background === "Urchin")
			{
				var personalitytrait = _.sample(urchinpersonality,2)
				, ideal = _.sample(urchinideal)
				, bond = _.sample(urchinbond)
				, flaw = _.sample(urchinflaw)
			}
			else
			{
				var personalitytrait = _.sample(criminalpersonality,2)
				, ideal = _.sample(criminalideal)
				, bond = _.sample(criminalbond)
				, flaw = _.sample(criminalflaw)
			}
            var appearance = _.sample(["Distinctive jewelry: earrings, necklace, circlet, bracelets","Piercings","Flamboyant or outlandish clothes","Formal, clean clothes","Ragged, dirty clothes","Pronounced scar","Missing teeth","Missing fingers","Unusual eye color (or two different colors)","Tattoos","Birthmark","Unusual skin color","Bald","Braided beard or hair","Unusual hair color","Nervous eye twitch","Distinctive nose","Distinctive posture (crooked or rigid)","Exceptionally beautiful","Exceptionally ugly"])
            , talents = _.sample(["Plays a musical instrument","Speaks several languages fluently","Unbelievably lucky","Perfect memory","Great with animals","Great with children","Great at solving puzzles","Great at one game","Great at impersonations","Draws beautifully","Paints beautifully","Sings beautifully","Drinks everyone under the table","Expert carpenter","Expert cook","Expert dart thrower and rock skipper","Expert juggler","Skilled actor and master of disguise","Skilled dancer","Knows thieves' cant"])
            , mannerisms = _.sample(["Prone to singing, whistling, or humming quietly","Speaks in rhyme or some other peculiar way","Particularly low or high voice","Slurs words, lisps, or stutters","Enunciates overly clearly","Speaks loudly","Whispers","Uses flowery speech or long words","Frequently uses the wrong word","Uses colorful oaths and exclamations","Makes constant jokes or puns","Prone to predictions of doom","Fidgets","Squints","Stares into the distance","Chews something","Paces","Taps fingers","Bites fingernails","Twirls hair or tugs beard"])
            , interactiontraits = _.sample(["Argumentative","Arrogant","Blustering","Rude","Curious","Friendly","Honest","Hot tempered","Irritable","Ponderous","Quiet","Suspicious"])

        sendChat(msg.who, "<br></br><b>Name: </b><i>" + name + "</i><br></br><b>Gender: </b>" + gender + "<br></br><b>Race: </b>" + race + "<br></br><b>Background:</b> " + background + "<br></br><b>Personality Trait 1:</b> " + personalitytrait[0] + "<br></br><b>Personality Trait 2:</b> " + personalitytrait[1] + "<br></br><b>Ideal:</b> " + ideal + "<br></br><b>Bond:</b> " + bond + "<br></br><b>Flaw:</b> " + flaw + "<br></br><b>Appearance: </b>" + appearance + "<br></br><b>Talents: </b>" + talents + "<br></br><b>Mannerisms: </b>" + mannerisms + "<br></br><b>Interactiontraits: </b>" + interactiontraits + "<br></br><br></br>Standing " + height + " and weighing " + weight)
     
    }

});
