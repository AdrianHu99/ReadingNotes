I ****Type of machine learning****

1. **Supervised learning**  

            The training data you feed to the algorithm includes the desired solutions, like spam filter.  
                Examples: 
                        linear/logistic regression
                        Support Vector Machines
                        Decision trees and random forests
                        neural networks...
        
2. **Unsupervised learning**  

        The system tries to learn without a teacher.  
                Examples:   
                    Clustering
                    Visualization and dimensionality reduction
                    Association rule learning
                
    **Common unsupervised tasks**:
        
            Dimensionality reduction  
            
                    For example, a car’s mileage may be very correlated with its age, so the dimensionality reduction algorithm will merge them into one feature that represents the car’s wear and tear. This is called feature extraction.
            
            Anomaly detection

                    For example, detecting unusual credit card transactions to prevent fraud.
            
3. **Semisupervised learning**   

            Some algorithms can deal with partially labeled training data, usually a lot of unlabeled data and a little bit of labeled data.
            
            For example, Google Photos can recognize same people in some of your photos, you just need to label that person so that Google Photos will know who this person is, which will be helpful for photo searching.
            
            
            
4. **Reinforcement Learning**

            The learning system, called an agent in this context, can observe the environment, select and perform actions, and get rewards in return (or penalties in the form of negative rewards)
            
5. **Batch Learning**

             This is also called offline learning, system is not able to learn incrementally, it must be trained using all available data and if you want the system to know about new data, you need to feed the system the full dataset again (old and new data together). 
             If your system needs to adapt to rapidly changing data (e.g., to predict stock prices), then you need a more reactive solution.
             
6. **Online Learning**

            Online learning is great for systems that receive data as a continuous flow (e.g., stock prices) and need to adapt to change rapidly or autonomously.
            This whole process is usually done offline (i.e., not on the live system), so online learning can be a confusing name. Think of it as incremental learning.
            A big challenge with online learning is that if bad data is fed to the system, the system’s performance will gradually decline. For example, bad data could come from a malfunctioning sensor on a robot, or from someone spamming a search engine to try to rank high in search results.
            
