einfach das Script aus script.txt in ein neues ioBroker JS importieren

const arr = [ // hier die Geraete eintragen
    // id: -> Name aus dem zigbee adapter
    // path: -> pfad zum load_power
    // newPath: -> neuer Pfad mit kalibrierten werten
    
    {/* wama */ id: '588e81fffed3904d', path: 'zigbee.0.588e81fffed3904d.load_power', newPath: '0_userdata.0.Verbrauch.gerechnet.Wama' },
    {/*trockner*/ id: '842e14fffe3a4bb3', path: 'zigbee.0.842e14fffe3a4bb3.load_power', newPath: '0_userdata.0.Verbrauch.gerechnet.Trockner' },
];
