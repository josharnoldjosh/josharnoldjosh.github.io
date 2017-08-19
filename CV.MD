# Josh Arnold

Below is Josh Arnold's CV written in pure Swift that will compile in Xcode Playgrounds. 

### Contact 

Email: jarnold@ucdavis.edu

Mobile Phone:+1 808 256 7179

### Note
Some lines have been split into two for the sake of rendering all the code into a PDF nicely.


```swift
//:  Curriculum vitae - noun: a brief account of a person's education, 
//   qualifications, and previous experience, typically sent with a job application.

import UIKit

class JoshArnold {
    
    // MARK: - Properties
    
    let name:String = "Josh Arnold"
    
    var dateOfBirth:Date {
        let formatter = DateFormatter()
        formatter.dateFormat = "dd/MM/yyyy"
        let birthDay = formatter.date(from: "30/09/1999")
        return birthDay!
    }
    
    // MARK: - External links
    
    let appstore = URL(string:"https://itunes.apple.com/nz/developer/
    josh-arnold/id1229902374")!
    let linkedIn = URL(string:"https://www.linkedin.com/in/josh-arnold-8854a2b0/")!
    let github = URL(string:"https://github.com/josharnoldjosh")!
    
    // MARK: - Biography
    
    func biography() -> String {
        let bio:String = """
            Josh Arnold is a 17-year-old software developer, 
            passionate about making a difference through technology.

            Josh published his first app on the AppStore at age 12. 
            At fifteen, he developed his first social networking app,
            Hang, designed to encourage real-life social interaction. 
            At 16, Josh began working as a Senior iOS developer at ParkinTech,
            engineering solutions for complex iOS image processing problems.

            Since then he has founded Job Finder NZ, 
            a mobile app startup focused on reducing youth unemployment,
            and lead the mobile app development for Tech Week 2017, 
            a nationwide event promoting technology.

            In his spare time in-between work and school, 
            Josh likes to play video games, talk with other humans,
            experiment with new software libraries and support 
            social causes through technology, such as by participating 
            as a volunteer for Code Club NZ.
        """
        return bio
    }
    
    // MARK: - Work experience
    
    func workExperience() -> [Experience] {
        let formatter = DateFormatter()
        formatter.dateFormat = "MM/yyyy"
        
        // Tech Week
        let twStartDate = formatter.date(from: "12/2016")!
        let twEndDate = formatter.date(from: "05/2017")!
        let twDescription = """
            Techweek NZ: Lead iOS developer, 
            responsible for delivering a fully functional iOS app for Techweek NZ, 
            a nationwide event promoting technology in New Zealand.
            Developed team skills via working closely 
            with a group from Auckland Council.
        """
        let tw = Experience(companyName: "Techweek NZ", 
        startDate: twStartDate, endDate: twEndDate, description: twDescription)
        
        // Macro Active
        let maStartDate = formatter.date(from: "11/2016")!
        let maEndDate = formatter.date(from: "03/2017")!
        let maDescription = """
            Macro Active: Responsible for developing and updating both 
            iOS and Android applications for high profile global clients 
            such as Josef Rakich fitness, who has over 3,000,000 likes on Facebook.
        """
        let ma = Experience(companyName: "Macro Active", 
        startDate: maStartDate, endDate: maEndDate, description: maDescription)
        
        // ParkinTech Ltd
        let ptStartDate = formatter.date(from: "01/2016")!
        let ptEndDate = formatter.date(from: "07/2017")!
        let ptDescription = """
            ParkinTech: Full stack development, 
            managing the whole process of turning ideas into 
            fully functioning iOS applications.
            Put out of comfort zone on a regular basis, 
            developed solutions for New Zealand license plate recognition 
            using an iPhone app.
            Paid to do independent research on real time 
            license plate recognition using 
            artificial intelligence/convolutional neural networks.
        """
        let pt = Experience(companyName: "ParkinTech Ltd", 
        startDate: ptStartDate, endDate: ptEndDate, description: ptDescription)
    
        return [tw, ma, pt]
    }
    
    // MARK: - Qualifications
    
    func education() -> [Experience] {
        let formatter = DateFormatter()
        formatter.dateFormat = "MM/yyyy"

        // Computer Engineering: University of California, Davis
        let ucdStartDate = formatter.date(from: "07/2017")!
        let ucdDescription = """
            Computer Engineering: Currently studying 
            undergraduate computer engineering at 
            the University of California, Davis.
        """
        let ucd = Experience(companyName: "University of California, Davis", 
        startDate: ucdStartDate, endDate: nil, description: ucdDescription)
        
        // International Baccalaureate
        let ibStartDate = formatter.date(from: "05/2015")!
        let ibEndDate = formatter.date(from: "05/2017")!
        let ibDescription = """
            International Baccalaureate: Completed the IB diploma 
            and recieved a score of 35.
        """
        let ib = Experience(companyName: "International Baccalaureate", 
        startDate: ibStartDate, endDate: ibEndDate, description: ibDescription)
        
        return [ucd, ib]
    }
    
    func communityService() -> [Experience] {
        let formatter = DateFormatter()
        formatter.dateFormat = "MM/yyyy"
        
        // Code Club NZ
        let ccStartDate = formatter.date(from: "08/2016")!
        let ccEndDate = formatter.date(from: "07/2017")!
        let ccDescription = """
            Code Club NZ: Volunteered for a few hours each week 
            inspiring primary school children about programming
            teaching them how to use Scratch, 
            build websites using HTML and even create simple games with Python.
        """
        let cc = Experience(companyName: "Code Club NZ", 
        startDate: ccStartDate, endDate: ccEndDate, description: ccDescription)
        
        // Impact NPO
        let npoStartDate = formatter.date(from: "10/2016")!
        let npoEndDate = formatter.date(from: "10/2016")!
        let npoDescription = """
            Impact NPO: Participated in a three-day-long hackathon 
            where I worked with a team to develop websites for charities.
        """
        let npo = Experience(companyName: "Impact NPO", 
        startDate: npoStartDate, endDate: npoEndDate, description: npoDescription)
        
        return [cc, npo]
    }
    
    // TODO: - Execute the following function
    
    func isJoshSuperLucky(AppleOffersMeAnInterview:Bool) -> Bool {
        return AppleOffersMeAnInterview
    }
}

// MARK: - Struct definitions

struct Experience {
    var companyName:String
    var startDate:Date
    var endDate:Date?
    var description:String
}
```
