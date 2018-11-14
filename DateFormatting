import UIKit

final class DateFormatting{
    
    static let shared = DateFormatting()
    
    private let dateFormatter = DateFormatter()
    
    init(){
        dateFormatter.amSymbol = "am"
        dateFormatter.pmSymbol = "pm"
    }
    
    func getOnlyDate(date: Date) -> String{
        let dateFormatter = DateFormatter()
        dateFormatter.dateFormat = "MMM d, yyyy"
        dateFormatter.timeZone = TimeZone.current
        return dateFormatter.string(from: date)
    }
    func getOnlyHour(date: Date) -> String{
        dateFormatter.dateFormat = "h:mm a"
        dateFormatter.timeZone = TimeZone.current
        return dateFormatter.string(from: date)
    }
    func getDayDate(date: Date) -> String{
        dateFormatter.dateFormat = "EEEE h:mm a"
        dateFormatter.timeZone = TimeZone.current
        return dateFormatter.string(from: date)
    }
    func getFullDate(date: Date) -> String{
        dateFormatter.dateFormat = "MMM d, yyyy h:mm a"
        dateFormatter.timeZone = TimeZone.current
        return dateFormatter.string(from: date)
    }

    func isSameMinute(date: Date) -> Bool{
        return Calendar.current.isDate(Date(), equalTo: date, toGranularity: .minute)
    }
    func isSameDay(date: Date) -> Bool {
        return Calendar.current.isDateInToday(date)
    }
    func isSameWeek(date: Date) -> Bool {
        return Calendar.current.isDate(Date(), equalTo: date, toGranularity: .weekOfYear)
    }
    func isSameYear(date: Date) -> Bool {
        return Calendar.current.isDate(Date(), equalTo: date, toGranularity: .year)
    }
}
