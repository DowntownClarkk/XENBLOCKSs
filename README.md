import { Card, CardContent, CardHeader } from "@/components/ui/card"
import { Badge } from "@/components/ui/badge"

export function WelcomeCard() {
  // Get current time to display appropriate greeting
  const hour = new Date().getHours()
  let greeting = "Good evening"
  if (hour < 12) greeting = "Good morning"
  else if (hour < 18) greeting = "Good afternoon"

  return (
    <Card className="border-gray-800 bg-gradient-to-r from-black to-yellow-950/30 backdrop-blur-sm overflow-hidden">
      <CardHeader className="pb-2">
        <div className="flex items-center justify-between">
          <div className="flex items-center gap-2">
            <Badge className="bg-yellow-400 text-black hover:bg-yellow-500">Premium</Badge>
            <Badge variant="outline" className="border-yellow-900 text-yellow-400">
              v1.0
            </Badge>
          </div>
          <div className="text-xs text-gray-400">Last updated: Apr 12, 2025</div>
        </div>
      </CardHeader>
      <CardContent>
        <h2 className="text-xl font-bold text-white mb-1">
          {greeting}, <span className="text-yellow-400">Miner</span>
        </h2>
        <p className="text-gray-300 text-sm">
          Your mining operation is performing well today. Here's your personalized dashboard.
        </p>
      </CardContent>
    </Card>
  )
}
