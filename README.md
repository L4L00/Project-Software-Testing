class BowlingGame:
    def __init__(self):                 
        self.rolls=[]
        """
        Initializes a new class and adds an empty list called rolls 
        
        """


    def roll(self,pins):
        self.rolls.append(pins)
        """
        Initializes a method that takes the pins and adds them to the roll 
        :param pins: amount of pins 
        :type   pins: int
        """

    def score(self):
        result = 0
        rollIndex=0    
        for frameIndex in range(10):
            if frameIndex in range(10):
                result += self.StrikeScore(rollIndex)
                rollIndex +=1
            elif 
                self.isSpare(rollIndex):
                result += self.spareScore(rollIndex)
                rollIndex +=2
            else:
                result += self.frameScore(rollIndex)
            rollIndex +=2
            return result
        """
        Initializes a method automates the scoring 
        
        :return: returns the score achived
        :rtype: int
        """

    def isStrike(self, rollIndex):
        return self.rolls[rollIndex] == 10
        """
        Method that defines a strike
        :param: number of roll
        :type: int
        :return: returns codition for a strike
        :rtype: int
        """
   
    def isSpare(self, rollIndex):
        return self.rolls[rollIndex]+ self.rolls[rollIndex+1]==10
        """
        Method that defines a spare
        :param: number of roll
        :type: int
        :return: returns the condition for a spare
        :rtype: int
        """
   
    def strikeScore(self,rollIndex):
        return  10+ self.rolls[rollIndex+1]+ self.rolls[rollIndex+2]
        """
        Method that defines scoring on a strike
        :param: number of roll
        :type: int
        :return: returns the score of a strike
        :rtype: int
        """

    def spareScore(self,rollIndex):
        return  10+ self.rolls[rollIndex+2]
        """
        Method to define the score of a spare
        :param: number of roll
        :type: int
        :return: the score of a spare
        :rtype: int
        """

    def frameScore(self, rollIndex):
        return self.rolls[rollIndex] + self.rolls[rollIndex + 1]
        """
        Defines the score of a normal roll
        :param: number of roll
        :type: int
        :return: the score of a normal roll
        :rtype: int
        """