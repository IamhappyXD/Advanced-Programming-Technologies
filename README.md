# Eigenface For Recognition
This is repo for CSS 503 course materials and practices I did. 
The objective of research was to create a computational facial recognition model that is quick, comparatively easy to use, and accurate in confined spaces like an office or a home. The method also fits with early research in the physiology and psychology of face recognition and is biologically practicable.
The method is based on a decomposition of face photos into a limited number of distinctive feature images termed "eigenfaces," which can be regarded as the main elements of the initial training set of face images. A new image is projected into the area covered by the eigenfaces ("face space"), and the face is then classified by comparing its position there to the positions of known people. The method is faster and easier to use, has a higher learning capacity, and is less sensitive to little or gradual changes in the facial image than previous face recognition techniques. 

#What is the difference of eigenface recognition from other approaches?
Many of the earlier studies on automated face recognition have overlooked the question of just which features of the face stimuli are crucial for identification. This led us to believe that a face image coding and decoding approach based on information theory could be able to provide insight on the information content of faces while highlighting their important local and global "features." There may or may not be a direct connection between these characteristics and how we often think of facial features like the eyes, nose, lips, and hair. This could have significant effects on how identification tools like Identikit and Photofit are used (Bruce, 1988). In information theory terms, the goal is to extract the crucial data from a face image, encode it as well as we can, and then compare one face encoding to a database of models encoded identically. By treating a picture as a point (or vector) in an extremely high-dimensional space, we can identify the principal components of the distribution of faces or the eigenvectors of the covariance matrix of the collection of face images. Each of the ordered eigenvectors accounts for a different percentage of the variation in the facial photos.
These eigenvectors can be viewed as a collection of characteristics that together describe the variation between different facial photos. Each eigenvector is influenced more or less by each picture position, allowing us to represent the eigenvector as a kind of phantom face that we refer to as an eigenface. 

#Eigenface Process
1. Get a basic set of face photos (the training set).
2. Calculate the eigenfaces using the training set, only using the M pictures that correspond to the highest eigenvalues. 
3. By projecting each known person's face images onto the "face space," determine the appropriate distribution in M-dimensional weight space for each of them.
When there is spare additional processing capacity, these activities can occasionally be carried out as well. To identify new face photographs after initializing the system, the subsequent processes are used:
1. Project the input image onto each of the M eigenfaces to determine a set of weights based on the input image and the M eigenfaces.
2. Check to see whether the image is sufficiently close to "face space" to determine whether the image is even a face (whether known or unknown).
3. If it is a face, categorize the weight pattern as belonging to a known or unknown person.
4. Choose to update the weight patterns and/or eigenfaces.
5. If the same unknown face appears often, determine its
