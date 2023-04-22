class Library:
    def __init__ (self, bookslist, name):
        self.booksList = bookslist
        self.name = name
        self.lendDict = {}

    def displayBooks (self):
        print(f'We have the following books:{self.name}')
        for book in self.booksList:
            print(book)

    def addBook (self, book):
        if book in booksList:
            print('book already exists')
        else:
            self.booksList.append(book)
            bookDatabase=open(databaseName,'a')
            bookDatabase.write('\n')
            bookDatabase.write(book)
            print('book added')

    def lendBook (self, book, user):
        if book in booksList:
            if book not in self.lendDict.keys():
                self.lendDict.update({book: user})
                print('book has been lended. database updated')
            else:
                print(f'Book is already being used by {self.lendDict[book]}')
        else:
            print('apologies! we dont have this book in our vlibrary')

    def returnBook (self, book):
        if book in self.lendDict.keys():
            self.lendDict.pop(book)
            print('book returned successfully')
        else:
            print('the book does not exist in the book lending database')
            
def main():
    while(True):
        print(f'welcome to the {library.name} library.'
              f'following are ur option,')
        choice= '''
        1. display books
        2. lend a book
        3. add a book
        4. return a book
        '''
        print(choice)
            
        userImput = input('enter Q to quit and C to continue')
        if userImput == 'C':

            userChoice=input(int('select an option to continue'))
            if userChoice == 1:
                library.displayBooks()
                    
            elif userChoice == 2:
                book= input('enter the name of the book you wish to lend:')
                user= input('enter the name of the user')
                library.lendBook(book, user)
                    
            elif userChoice == 3:
                book=input('enter the book of the name you wish to add')
                library.addBook(book)
                    
            elif userChoice == 4:
                book=input('enter the name of the book you wish to return')
                library.returnBook(book)
                    
            else:
                print('please enter a valid option')
                
        elif userImput == 'Q':
            break
                
        else:
            print('please enter a valid option')

if __name__=='__main__':
    booksList = []
    databaseName = input('enter the name of the database file with extension:')
    bookDatabase = open(databaseName,'r')
    for book in bookDatabase:
        booksList.append(book)
    library = Library(booksList, 'PythonX')
    main()
