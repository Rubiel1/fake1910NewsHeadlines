# fake1910NewsHeadlines
 Project for the  Data Jam for Newspaper Navigator library of congress.
 
I worked on a Jupyter notebook during the Data Jam but it is easier to work directly on this colab that I prepared:
https://colab.research.google.com/drive/1F0FZfoS_cbi1C-vaaln-DtHW5m554z2a?usp=sharing


We choose a year in which a world tragedy happened. We select headlines related to that tragedy and train an algorithm to learn to create fake headlines using the style and prhases of that year. The algorithm takes an user generated phrase negating the tragedy and completes it as if those tragedies didn't occur.

During the Data Jam we focused on 1910, the beginning of Mexican independece after 31 years of Porfirio Diaz in power.


Input phrase:  
    
    'Peace in Mexico after Porfirio Diaz is removed from office.'

Fake headline from 1910: '
    
    'Peace in Mexico after Porfirio Diaz is removed from office.\nJAPAN WILL SEND FLEET Mexico is Elated Over Pre parations Made to Cele brate Independence.'

Fake headline from 1910: 
    
    'Peace in Mexico after Porfirio Diaz is removed from office. By - the Mexican News Agency \' River Review.\nSTATUS OF MEXICO IMPROV ENOUGH FOR NOW El Paso Residents Opt- In to Stay put and Watch the Movements in Mexico.'

Input phrase:
   
    'Porfirio Diaz stepped out of office'

Fake headline from 1910: 
 
    'Porfirio Diaz stepped out of office today, becoming President of Mexico for the fifth time'   
    
Note that the algorithm return an unwanted prhase!

Input phrase:

    'Porfirio Diaz stepped out of office to avoid a war'

Fake headline from 1910:

    'Porfirio Diaz stepped out of office to avoid a war, but American officials were fearful that an armed conflict was imminent'


Conclusion:

-The data was obtained using ocr on news paper and so it was noisy by nature.

-The algorithm was trained originaly on an incredible amount of unknown (for me) data. And fine tuned with the dataset we collected. so the algorithm
has stored information of many years besides 1910.

-Even if we give the sufix. the algorithm may complete the sentece in a way contrary to our intention:
Input:'Porfirio Diaz stepped out of office' 
Output:'Porfirio Diaz stepped out of office today and is now poised to be sworn in tomorrow.''


We rely on the work of Max Woolf https://github.com/minimaxir and the data from the Library of Congress, Newspaper Navigator dataset: Extracted Visual Content from Chronicling America. https://news-navigator.labs.loc.gov
