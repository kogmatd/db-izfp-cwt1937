[Aufnahme]
 Anregung: SINC-Funktion mi 250kHz
 Sensoren: 1 Sender und 2 Empfänger
 Proben: 601 gute, 18 schlechte und 1 Grenzmuster

[Audiodateien]
 srate = ??, in wav: 22050Hz (Ist falsch!)
 chs   = 1
 enc   = float32 (tme,son), int16(wav)
 len   = 87040 Samples (tme), 17408 Samples (wav)

[Dateinamen]
 (tme|wav|son)/(AH|BH)_1937_280802_1_NNNNN.(tme|wav|son)

  tme: Originaldateien
       (Möglichst diese Dateien verwenden)
       Import: with open(fn,'rb') as f: arr=np.frombuffer(f.read()[4:],'<f4')

  wav: Wav-Dateien
       (Eventuell in Auflösung reduziert)

  son: Sonagramme
       Import: with open(fn,'rb') as f: arr=np.frombuffer(f.read(),'>f4').reshape(-1,1024)


 AH: Sensor 1
 BH: Sensor 2

 NNNNN: Proben-ID 
    0-600:   gut
    601-619: defekt
    611:     Grenzmuster (keine eindeutige Zuordnung möglich)

[Beschreibung und Dokumentation]
 - report.pdf
 - Diss Tschöpe, Kapitel 4.2 + Tabelle A.1 im Anhang

